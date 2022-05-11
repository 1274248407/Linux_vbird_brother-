# Regular Express (RE)
## 11.4 sed tool
```
DOS format              Unix format
"Edit.^M$"              "Edit.$"

sed -i 's/\.$/\!\g' "Edit.Unix.format"
'/.$' divide below:
	Text: '\.' = '.'
	$: asserts position at the end of a line
result: "Edit!$"

sed -i 's/\.$/\!\g' "Edit.DOS.format"
	"Edit.^M$" 
	'\.' + '^M' + '$' in DOS format
	'\.' + '$' in the Regular express it is not match
	result: "Edit.^M$"		nothing change

correct: sed -i 's/\..$/\!\g' "Edit.Unix.format"
'/..$' divied below:
	Text: '\.' = '.'
	'.': match any character (expect for line terminators)
	$: asserts position at the end of a line
	'.' + '^M' + '$' in DOS format
	'\.' + '.'  + '$' in the Regular express
	it is match
result: "Edit!$"
```
-----------
## 11.4.2 awk
```bash
cat pay.txt | 
 > awk 'NR==1{printf "%10s %10s %10s %10s %10s\n",$1,$2,$3,$4,"Total" } \
 > NR>=2{total = $2 + $3 + $4; \
 > printf "%10s %10d %10d %10d %10.2f\n", $1, $2, $3, $4, total}'
```
**total = $2 + $3 + $4; same as c **. add ';'

 




	