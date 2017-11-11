ITM0-556

Lab week 11 - chap 8


1) declare -a itemARRAY

2) the code:
```bash

mapfile -t diraar < <(ls -l ~)
echo ${diraar[2]}
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
![capture d ecran 2017-11-10 a 11 31 52](https://user-images.githubusercontent.com/27293298/32670885-d5c46690-c60a-11e7-8468-c0ce1ec0104e.png)


6) $1 = /datapool1 , i replace every occurence in path and my loops of /datapool1 by $1. Then i passed /datapool as the first positional parameter

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
    exit;
    
fi
```
output :
![capture d ecran 2017-11-10 a 11 36 57](https://user-images.githubusercontent.com/27293298/32671056-7fd097da-c60b-11e7-83ef-f7b6595dc510.png)



9)


