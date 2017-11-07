ITM0-556

Lab week 11 - chap 8


1) declare -a itemARRAY

2) the code:
```bash

mapfile -t diraar < <(ls -l ~)
echo ${diraar[3]}
echo ${diraar[3]}

```
the result: 
![capture d ecran 2017-11-07 a 13 03 29](https://user-images.githubusercontent.com/27293298/32512276-1cc58214-c3bc-11e7-9023-80a097c95df3.png)

3) the code:
```bash

mapfile -t diraar < <(ls -l ~)
length=${#diraar[@]}
echo $length

for ((i=0 ; i<$length ; i++))
  do 
    echo ${diraar[$i]}
  done
```
the result : ![capture d ecran 2017-11-07 a 13 18 41](https://user-images.githubusercontent.com/27293298/32512940-32ab1a56-c3be-11e7-8670-1f14c8e1b53b.png)

4) 5 * * * *

5)
![capture d ecran 2017-11-07 a 13 39 21](https://user-images.githubusercontent.com/27293298/32513901-227214a2-c3c1-11e7-88a8-9e264d0fae9f.png)

6)  !!!!!!! 
```bash
$1: $PATH
```

7)
```bash
if [ $# != 1]
  then
    echo "there is exactly one positional parameter"
else 
    echo "there is either 0 or more than 1 position parameter"
    exit;
fi
```
8)
```bash
if [ -a $1 && -x ]
  then
    echo "file exists and is executable"
else 
    echo "the positional parameter is not executable"
    
fi
```
output :
![capture d ecran 2017-11-07 a 13 39 21](https://user-images.githubusercontent.com/27293298/32516594-707e0888-c3c9-11e7-832c-31d4959bca65.png)


9)

