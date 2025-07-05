<type>
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd
3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold
5) **Price**: positive value representing the price of the security
6) **Commision**: negative value representing commision charges
7) **Total Quantity**: total quantity of shares
8) **Realized PnL**: total realized profit/lost

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665
ORCL   | 2024-06-11 |  16:10:24 |     10 |  132.691 | -1.000 |    20 |   -183.665
ORCL   | 2024-06-11 |  16:12:58 |     10 |  135.970 | -1.000 |    30 |   -183.665
ORCL   | 2024-06-11 |  16:16:47 |   -100 |  135.120 | -1.392 |   -70 |    -90.061

ASSUMPTIONS:

1) the number of **buys records** and **sell records** is random 
2) the given data is already sorted by date and time.
3) for any record, a positive quantity in  the 4th field (Quantity) 
   represents a **buy**, a negative represents a **sell**.

PROCESS OVERVIEW:

The program will compare and process two consecutive records 
sequentially.

Two arrays could be use to parcel and store the fields of two
consecutive records; name them "record_current" and "record_next".

The script compares **two consecutive records at a time** (e.g.: 1 & 2, 
2 & 3, 3 & 4, 4 & 5, etc.) using the quantity (4th field) as comparison 
criteria.

If the current pair of sequential records (e.g.: 1 & 2) are both 
**buy** or both **sell**, put "record_current" in a buffer and move 
to the next pair of record (e.g.: 2 & 3) without further processing.

If the field **Quantity** of each record are opposites of each other 
(i.e., 25 shares bought and -25 shares sold), they cancel each other 
out; this records are ignored and nothing is store in the buffer. Next,
the sequential process move **two** records down, (e.g.: if records 
3 & 4 cancel out, we move to 5 & 6, not 4 & 5)

If the magnitude of the field **Quantity** in "record_current" is 
larger, then updated its field **Quantity** with the sum of fields 
**Quantity** from both records. Also, its field **Total Quantity** 
(the 7th field) must be updated buy adding the **Quantity** from 
"record_next" to it. Finally, add the record "record_current" into 
the buffer.

If the magnitude of the field **Quantity** in "record_next" is 
larger, then updated its field **Quantity** with the sum of fields 
**Quantity** from both records. Also, its field **Total Quantity** 
(the 7th field) must be updated buy adding the **Quantity** from 
"record_current" to it. Finally, add the record "record_next" into 
the buffer.

The algorithm always retained the **commission** and **realized PnL** 
of the record containing the **Quantity** with the larger magnitude of
the current two records.

The buffer is then re-processed using the previous algorithm until 
there are no more mixed positions; i.e.: all records in the buffer 
should be **buys** or **sells**, but not both.

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
</type>

Let's break down these instructions.

### 1) Questions the Instructions Could Have Left Unanswered:

* **What is the ultimate goal or purpose of this processing?** While it describes the steps, it doesn't state *why* this specific reconciliation/consolidation of records is being performed. Is it for portfolio tracking, PnL calculation, simplifying trade history, or something else? Understanding the objective could help validate the logic.
* **What should happen if the input data is empty or contains only one record?** The "process overview" assumes at least two records for comparison.
* **What happens if `record_current` and `record_next` have the same `Symbol`, but different `Date` or `Time` for the same trade?** The sample input shows records for "ORCL" across different dates and times. The current logic seems to imply that only records with *opposite quantities* but *the same stock* will be considered for cancellation/consolidation. Is it possible for trades of the same stock on different days/times to offset each other, or should the processing be grouped by symbol first? The instructions imply sequential processing through a single stream of records, regardless of symbol, but the sample data is all for one symbol.
* **Clarification on "mixed positions" for the final buffer processing:** The instruction states, "The buffer is then re-processed using the previous algorithm until there are no more mixed positions; i.e.: all records in the buffer should be buys or sells, but not both." This implies that after the first pass, the buffer might still contain alternating buys and sells that need further consolidation. This recursive/iterative processing needs to be clear about how the "pair of sequential records" is determined within the buffer, especially if records were skipped in the initial pass.
* **What if the `Quantity` field values are not exact opposites (e.g., 25 shares bought and -20 shares sold)?** The current rule says "if the field Quantity of each record are opposites of each other (i.e., 25 shares bought and -25 shares sold), they cancel each other out." It doesn't specify what to do if magnitudes don't exactly match for a full cancellation. The subsequent rules about larger/smaller magnitudes seem to handle *partial* offsets, but the "cancel out" rule is very strict. It seems that the "cancel out" rule (exact opposites) takes precedence over the magnitude comparison rules, but this needs to be confirmed for partial overlaps. Given the later rules about "sum of fields Quantity" for larger magnitudes, it strongly implies partial offsets are handled by those rules, making the "exact opposites" rule redundant or needing clarification on its priority if partials are handled.
* **Clarification on "Realized PnL" and "Commission" for the combined record:** The instructions say, "The algorithm always retained the commission and realized PnL of the record containing the Quantity with the larger magnitude of the current two records." This is unusual for financial calculations. Typically, when quantities are combined (even if one is negative, meaning an offset), the PnL and Commission should be *summed* or *calculated proportionally* based on the combined trade, not simply retaining one. This needs confirmation if this simplified approach is truly desired.
* **What happens to records that are "put in a buffer" but never explicitly processed again?** If two consecutive records are both buys/sells, the "record_current" is put in a buffer. But then the loop moves to the *next pair*. Does `record_next` from the previous pair become `record_current` for the new pair? How does the processing ensure that `record_next` (which was a buy/sell and not handled) doesn't get lost or handled incorrectly in the subsequent iteration?

### 2) Rewritten Instructions (Concise and with Answers to Questions):

**Objective:** Consolidate sequential stock buy/sell records with a focus on netting offsetting positions and aggregating same-direction trades, ultimately producing a filtered list of reconciled trades. This process is applied iteratively until no further netting or aggregation is possible within the buffer.

**Input Data:** Pipe-separated records (`|`) for stock trades, sorted by date and time. Each record has:
1.  **Symbol** (string)
2.  **Date** (YYYY-MM-DD)
3.  **Time** (HH:MM:SS)
4.  **Quantity** (integer; positive for buy, negative for sell)
5.  **Price** (float; positive)
6.  **Commission** (float; negative)
7.  **Total Quantity** (integer)
8.  **Realized PnL** (float)

**Process:**

1.  **Initialize Buffer:** Start with an empty buffer.
2.  **Iterative Processing:** Process the input records (and later, the buffer) in consecutive pairs (`record_current`, `record_next`) until no more changes occur. The records in the input are assumed to belong to the *same stock symbol* for comparison purposes. Handle empty input or single records by simply returning them (or an empty set).

3.  **Pair Comparison Logic:**
    * **Same Direction (Both Buy or Both Sell):** If `record_current.Quantity` and `record_next.Quantity` have the same sign (both positive or both negative), add `record_current` to the buffer without further modification. Then, move to the next pair: `record_next` becomes the new `record_current`, and the record following it becomes `record_next`. (This implies `record_next` effectively *skips* an evaluation in the current pass).
    * **Opposite Quantities (Offsetting Trades):** If `record_current.Quantity` and `record_next.Quantity` have opposite signs and their *absolute magnitudes are equal* (e.g., 25 and -25), these two records fully cancel each other out. **Ignore both records** for the buffer. Advance processing by **two** records (i.e., `record_next.next` becomes the new `record_current`).
    * **Opposite Quantities (Partial Offset/Aggregation):** If `record_current.Quantity` and `record_next.Quantity` have opposite signs, but their absolute magnitudes are *unequal*:
        * **Determine Dominant Record:** Identify the record with the larger *absolute magnitude* of `Quantity`.
        * **Update Dominant Record:**
            * Set the `Quantity` of the dominant record to the algebraic sum of `record_current.Quantity` and `record_next.Quantity`. (e.g., if current is 50, next is -20, dominant becomes 30. If current is 20, next is -50, dominant becomes -30).
            * Update the `Total Quantity` of the dominant record by adding `record_next.Quantity` to it.
            * **Retain `Commission` and `Realized PnL`:** The `Commission` and `Realized PnL` of the dominant record are kept as they are; they are *not* summed or recalculated from both records.
        * **Add to Buffer:** Add the **updated dominant record** to the buffer.
        * **Advance Processing:** Move to the next pair, similar to the "Same Direction" case: the record following `record_next` becomes the new `record_current`.

4.  **Buffer Re-processing:** After an initial pass through all input records, the generated buffer becomes the new set of records to be processed. Repeat the "Pair Comparison Logic" (steps 2 and 3) on the buffer. Continue this iterative re-processing until a pass through the buffer results in no further changes (i.e., all remaining records are either exclusively buys or exclusively sells, not a mix).

**Output:** Print all records in the final, consolidated buffer using the original pipe-separated format. If the input was empty or resulted in no records after processing, print nothing.
