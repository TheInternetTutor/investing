# List of supported languages and lexers
### https://github.com/rouge-ruby/rouge/wiki/List-of-supported-languages-and-lexers

## Favorite Themes:
```scala
ceylon         crystal        dart
elixir         elm            gradle
groovy         haskell        kotlin
matlab         moonscript     rust
scala          smalltalk      vala
yaml
```

## Languages:
```scala
abap              actionscript      apache            apiblueprint      applescript       
awk               biml              brainfuck         bsl               c                 
ceylon            cfscript          clojure           cmake             coffeescript      
common_lisp       conf              console           coq               cpp               
crystal           csharp            css               d                 dart              
diff              digdag            docker            dot               eiffel            
elixir            elm               erb               erlang            escape            
factor            fortran           fsharp            gherkin           glsl              
go                gradle            graphql           groovy            hack              
haml              handlebars        haskell           hcl               html              
http              hylang            idlang            igorpro           ini               
io                irb               java              javascript        jinja             
json              json-doc          jsonnet           jsp               jsx               
julia             kotlin            lasso             liquid            literate_coffeescript
literate_haskell  llvm              lua               m68k              magik             
make              markdown          mathematica       matlab            moonscript        
mosel             mxml              nasm              nginx             nim               
nix               objective_c       ocaml             pascal            perl              
php               plaintext         plist             powershell        praat             
prolog            prometheus        properties        protobuf          puppet            
python            q                 qml               r                 racket            
ruby              rust              sass              scala             scheme            
scss              sed               shell             sieve             slim              
smalltalk         smarty            sml               sqf               sql               
supercollider     swift             tap               tcl               terraform         
tex               toml              tsx               tulip             turtle            
twig              typescript        vala              vb                verilog           
vhdl              viml              vue               wollok            xml               
xojo              yaml              
```

```abap
LANGUAGE: abap
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```actionscript
LANGUAGE: actionscript
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```apache
LANGUAGE: apache
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```apiblueprint
LANGUAGE: apiblueprint
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```applescript
LANGUAGE: applescript
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```awk
LANGUAGE: awk
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```biml
LANGUAGE: biml
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```brainfuck
LANGUAGE: brainfuck
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```bsl
LANGUAGE: bsl
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```c
LANGUAGE: c
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```ceylon
LANGUAGE: ceylon
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```cfscript
LANGUAGE: cfscript
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```clojure
LANGUAGE: clojure
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```cmake
LANGUAGE: cmake
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```coffeescript
LANGUAGE: coffeescript
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```common_lisp
LANGUAGE: common_lisp
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```conf
LANGUAGE: conf
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```console
LANGUAGE: console
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```coq
LANGUAGE: coq
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```cpp
LANGUAGE: cpp
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```crystal
LANGUAGE: crystal
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```csharp
LANGUAGE: csharp
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```css
LANGUAGE: css
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```d
LANGUAGE: d
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```dart
LANGUAGE: dart
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```diff
LANGUAGE: diff
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```digdag
LANGUAGE: digdag
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```docker
LANGUAGE: docker
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```dot
LANGUAGE: dot
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```eiffel
LANGUAGE: eiffel
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```elixir
LANGUAGE: elixir
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```elm
LANGUAGE: elm
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```erb
LANGUAGE: erb
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```erlang
LANGUAGE: erlang
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```escape
LANGUAGE: escape
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```factor
LANGUAGE: factor
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```fortran
LANGUAGE: fortran
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```fsharp
LANGUAGE: fsharp
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```gherkin
LANGUAGE: gherkin
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```glsl
LANGUAGE: glsl
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```go
LANGUAGE: go
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```gradle
LANGUAGE: gradle
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```graphql
LANGUAGE: graphql
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```groovy
LANGUAGE: groovy
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```hack
LANGUAGE: hack
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```haml
LANGUAGE: haml
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```handlebars
LANGUAGE: handlebars
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```haskell
LANGUAGE: haskell
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```hcl
LANGUAGE: hcl
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```html
LANGUAGE: html
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```http
LANGUAGE: http
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```hylang
LANGUAGE: hylang
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```idlang
LANGUAGE: idlang
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```igorpro
LANGUAGE: igorpro
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```ini
LANGUAGE: ini
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```io
LANGUAGE: io
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```irb
LANGUAGE: irb
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```java
LANGUAGE: java
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```javascript
LANGUAGE: javascript
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```jinja
LANGUAGE: jinja
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```json
LANGUAGE: json
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```json-doc
LANGUAGE: json-doc
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```jsonnet
LANGUAGE: jsonnet
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```jsp
LANGUAGE: jsp
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```jsx
LANGUAGE: jsx
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```julia
LANGUAGE: julia
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```kotlin
LANGUAGE: kotlin
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```lasso
LANGUAGE: lasso
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```liquid
LANGUAGE: liquid
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```literate_coffeescript
LANGUAGE: literate_coffeescript
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```literate_haskell
LANGUAGE: literate_haskell
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```llvm
LANGUAGE: llvm
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```lua
LANGUAGE: lua
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```m68k
LANGUAGE: m68k
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```magik
LANGUAGE: magik
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```make
LANGUAGE: make
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```markdown
LANGUAGE: markdown
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```mathematica
LANGUAGE: mathematica
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```matlab
LANGUAGE: matlab
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```moonscript
LANGUAGE: moonscript
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```mosel
LANGUAGE: mosel
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```mxml
LANGUAGE: mxml
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```nasm
LANGUAGE: nasm
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```nginx
LANGUAGE: nginx
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```nim
LANGUAGE: nim
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```nix
LANGUAGE: nix
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```objective_c
LANGUAGE: objective_c
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```ocaml
LANGUAGE: ocaml
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```pascal
LANGUAGE: pascal
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```perl
LANGUAGE: perl
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```php
LANGUAGE: php
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```plaintext
LANGUAGE: plaintext
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```plist
LANGUAGE: plist
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```powershell
LANGUAGE: powershell
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```praat
LANGUAGE: praat
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```prolog
LANGUAGE: prolog
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```prometheus
LANGUAGE: prometheus
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```properties
LANGUAGE: properties
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```protobuf
LANGUAGE: protobuf
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```puppet
LANGUAGE: puppet
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```python
LANGUAGE: python
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```q
LANGUAGE: q
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```qml
LANGUAGE: qml
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```r
LANGUAGE: r
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```racket
LANGUAGE: racket
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```ruby
LANGUAGE: ruby
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```rust
LANGUAGE: rust
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```sass
LANGUAGE: sass
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```scala
LANGUAGE: scala
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```scheme
LANGUAGE: scheme
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```scss
LANGUAGE: scss
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```sed
LANGUAGE: sed
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```shell
LANGUAGE: shell
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```sieve
LANGUAGE: sieve
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```slim
LANGUAGE: slim
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```smalltalk
LANGUAGE: smalltalk
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```smarty
LANGUAGE: smarty
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```sml
LANGUAGE: sml
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```sqf
LANGUAGE: sqf
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```sql
LANGUAGE: sql
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```supercollider
LANGUAGE: supercollider
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```swift
LANGUAGE: swift
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```tap
LANGUAGE: tap
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```tcl
LANGUAGE: tcl
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```terraform
LANGUAGE: terraform
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```tex
LANGUAGE: tex
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```toml
LANGUAGE: toml
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```tsx
LANGUAGE: tsx
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```tulip
LANGUAGE: tulip
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```turtle
LANGUAGE: turtle
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```twig
LANGUAGE: twig
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```typescript
LANGUAGE: typescript
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```vala
LANGUAGE: vala
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```vb
LANGUAGE: vb
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```verilog
LANGUAGE: verilog
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```vhdl
LANGUAGE: vhdl
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```viml
LANGUAGE: viml
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```vue
LANGUAGE: vue
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```wollok
LANGUAGE: wollok
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```xml
LANGUAGE: xml
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```xojo
LANGUAGE: xojo
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
```yaml
LANGUAGE: yaml
INPUT:

The input data is related to random buys and/or sell records related to 
stocks securities. Each record contains eight fields separated by the 
pipe character '|'. Description of each field is a follows:
1) **Symbol**: security symbol or ticker
2) **Date**: date in the format yyyy-mm-dd 3) **Time**: time in the format hh:mm:ss
4) **Quantity**: amount of shares bought or sold

Sample input:
ORCL   | 2024-06-03 |  15:59:51 |      5 |  119.225 | -1.000 |     5 |   -253.543
ORCL   | 2024-06-05 |  09:58:15 |     10 |  121.000 | -1.000 |    15 |   -253.543
ORCL   | 2024-06-07 |  15:53:41 |    -15 |  125.270 | -1.055 |     0 |   -183.665
ORCL   | 2024-06-11 |  16:06:53 |     10 |  129.150 | -1.000 |    10 |   -183.665

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

OUTPUT:

Finally print all the records in the buffer using the original format
in the input.
```
---
