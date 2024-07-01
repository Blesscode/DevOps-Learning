# Yaml
- It is used to represent data and convert in any object

## pairs in yaml
- In Yaml we have everything in key value format key: value
- name : "isha"
- 1 : "name"
- # ALTERNATIVE:
  - {1: "name", name: "isha"}  
## list
- item1
- item 2

## block
- eg. 
  cities:
    - lucknow
    - delhi 
- # ALTERNATIVE:
  - cities: [lko,delhi]  //array  

## Yaml is case sensitive
-apple
-Apple

## In yaml we use spaces and indentaion is very important
-you can check indentaion using yaml parser

## how to seperate the document 
- use --- after every document(eg. after a list or a block or key val pairs) end

## end document
- use ...

<hr>

# 2. Datatypes

name: variable
## string variable
- yaml has 3 types
pronounes: Her
Name : "Isha"
Address: 'secret'

{treat ever line a one}
bio:
I am a nice person
I enjoy everyone's company 

- Write a single line in multiple line
message: >
line 1
line 2
line 3

## numbers
 
number: 123
marks: 98.28
booleanValues : No // n,N,false,False

## Specify the type
- Yaml can tell the datatype using
## Integers= zero: !!datatype value
- eg. 
zero: !!int 0
positiveNo: !!int 45
negativeNo: !!int -45
binaryNo: !!int 0b11001
octalNo: !! 06574
commaValue: !!int +540_000 //540,000

# float no
marks: !!float 1.56
infinity: !!float .inf
not a number: .nan

## null
surname: !!null Null // or null Null ~
~: this is a null key
## date and time in yaml
date: !!timestamp 02-06-2023
india time: 2001-12-15T02:59:43.10 +5:30

<hr>

# Adv datatypes
## 1 sequence (seq)

student: !!seq
-marks
-name
-roll_no

//alternative cities: [lko,delhi]
// i empty sequence key /*sparse seq*/
sparese seq:
-hey
-how
-
-Null
//ii nested items (use one - command to do so)
-
  -first name
  -last name
-phone_no 

## map
// Key: vale pair uses map
!!map

//nested mapping
name: isha
role:
  age: 64
  job: student
//alternative role: {age:64,job:student}

## pairs
-key may have dublicate values
!!pairs

pair example: !!pairs
 - job: student
 - job: teacher
 //this is an array of hashtables
 //alernative pair example: !!pairs[job:student,job: teacher] 

 ## set
 - allow only for unique keys
 - no key value only key
 name:!!set
 ? isha
 ? ish

 ## dictionary !!omap
 -sequence as value
 people: !!omap
  - isha:
     name: isha gupta
     age:64
  - ish
     name:ish gupta
     age:65

## reusing some properties- use anchors
liking: &likes
  fav fruits:apple
  dislike:jackfruit

person1:
  name:isha
  <<: *likes
person2:
  name:ish
  <<: *likes
  dislikes: mango //overriding properties

<hr>

# Real life example in 3 types
- xml
- JASON
- yaml

## check for valid yaml
[Validate your yaml link](https://www.yamllint.com/)







