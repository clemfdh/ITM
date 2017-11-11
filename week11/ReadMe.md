ITM0-556

Lab week 11 - chap 8


# 1 #
declare -a itemARRAY 

# 2 #
the code:
```bash

mapfile -t diraar < <(ls -l ~)
echo ${diraar[2]}
echo ${diraar[3]}

```
the result: 
![capture d ecran 2017-11-07 a 13 03 29](https://user-images.githubusercontent.com/27293298/32512276-1cc58214-c3bc-11e7-9023-80a097c95df3.png)

# 3 # 
the code:
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

# 4 #
5 * * * * /our/path.sh

# 5 #
![capture d ecran 2017-11-10 a 11 31 52](https://user-images.githubusercontent.com/27293298/32670885-d5c46690-c60a-11e7-8468-c0ce1ec0104e.png)


# 6 #
$1 = /datapool1 , i replace every occurence in path and my loops of /datapool1 by $1. Then i passed /datapool as the first positional parameter

# 7 #
```bash
if [ $# != 1]
  then
    echo "there is exactly one positional parameter"
else 
    echo "there is either 0 or more than 1 position parameter"
    exit;
fi
```
# 8 #
```bash
if [ -x $1 ]
  then
    echo "file exists and is executable"
else 
    echo "the positional parameter is not executable"
    exit;
    
fi
```
output :
![capture d ecran 2017-11-11 a 10 38 03](https://user-images.githubusercontent.com/27293298/32691381-73a81660-c6cc-11e7-8783-db4940edcbde.png)



# 9 #
To do so i used the positional parameter. So the user would just give the name of a file and by executing the script it will tell him if it exists.
```bash
name=$1
if [ -f "$name"]
  then
    echo "the file with the name : $name exists "
  else
    echo "there is no file with the name : $name"
    exit;
fi
```

console output: 
![capture d ecran 2017-11-11 a 10 52 56](https://user-images.githubusercontent.com/27293298/32691559-11c165ca-c6cf-11e7-9480-99e12a4874a7.png)


# 10 #
```bash
PATH=$1
if [ -d $PATH ]
  then
    echo "$PATH is a directory"
elif [ -f $PATH ]
  then
    echo "$PATH is a file"
else 
  echo "$PATH is nothing"
  exit;
fi
```
console output:
![capture d ecran 2017-11-11 a 11 41 57](https://user-images.githubusercontent.com/27293298/32691967-abc62600-c6d5-11e7-9068-9d622c35d503.png)

# 11 #
```bash

echo "This is the first positional parameter (the file itself): $0"
echo "This is the length of the number of positional parameters (not counting \$0): $#"
echo "This is tall the parameters: $@"
```
console output: 
![capture d ecran 2017-11-11 a 11 53 16](https://user-images.githubusercontent.com/27293298/32692077-53cd4af8-c6d7-11e7-8c3f-25883d8fcb3c.png)

# 12 #
i open crontab -e. then i edit the document as follow: 

5 * * * * /our/path.sh >> ~/Docments/my.log 2>&1


