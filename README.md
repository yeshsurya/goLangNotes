# goLangNotes
Short notes of golang


<ul>
<li>
Multiple *.go files can be grouped under a notion of “package name” </li>
</br>
Two types of packages are 1. Reusable 2. Executable
word “main” is used to make executable type package
for executable type package you’ll need to have a function with name “main”
“fmt” - shortened form of format
“Go” is a statically typed language
Basic go datatype : 1. string 2. int 3. float64 4. bool
Variable type inference syntax : 
cards := “Ace of Spades”
equivalent to  var cards string = “Ace of Spades”
Return type in function declaration : 
func functionName() string{
	return “Ace of Cards”
}
Functions defined in other files are visible to present file if they are part of same package.
“Array” is fixed length list 
“Slice” is dynamic length list
Elements of Array or Slice should be of same datatype
Slice example : 
cards := []string{“first”,”second”}
cards = append(cards,”third”)
for i,card := range cards{
       fmt.Println(i,card)
}
Inside the for loop both i,card should be used ; else we’ll get an error ; But when u don’t want to use it we’ll replace it with underscore (_)
Receiver functions in golang : 
type deck []string
func (d deck) print(){
   for i,card := range d{
        fmt.Println(i,card)
   }
As a convention go avoids any mention of “this” and “self”
Slicing on a slice data type is same as in python i.e like array[0:2] , array[:2] , array[2:]
function can return multiple values : 
Example : 
func (d deck) returnMulti(d deck , handleDeck int) ( deck , deck) {
     return d[handleDeck:],d[:handleDeck]
}

Converting strings to byte stream : 
fmt.Println([]byte”Hello World”)
Importing multiple packages : 
Import (
“fmt”
“strings”
)
Saving to a file
ioutil.WriteFile(“filename1.txt”,[]byte(obj.toString()),0666)
The way to get the length of the slice is “len(sllice_variable_name”)”

</ul>
