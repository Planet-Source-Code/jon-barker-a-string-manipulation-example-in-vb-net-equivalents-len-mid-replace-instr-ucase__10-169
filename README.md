<div align="center">

## \_ A String manipulation example in VB\.NET, EQUIVALENTS: Len, Mid, Replace, InStr, UCase, Split etc \_


</div>

### Description

A string manipulation example in VB.NET.

Are ALL covered in the tutorial, using PURE VB.NET STRING MANIPULATION TEQNIQUES

Commands and equivilents

Len = .Length,

Mid = .SubString,

Replace = .Replace,

InStr = .IndexOf,

UCase = .ToUpper,

LCase = .ToLower,

Split = .Split,

Join = .Join,

Enjoy! tHe_cLeanER
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Jon Barker](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/jon-barker.md)
**Level**          |Beginner
**User Rating**    |4.6 (399 globes from 87 users)
**Compatibility**  |VB\.NET
**Category**       |[Strings](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/strings__10-26.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/jon-barker-a-string-manipulation-example-in-vb-net-equivalents-len-mid-replace-instr-ucase__10-169/archive/master.zip)





### Source Code

<html><head><title>String manipulation in VB.NET. Equivalents of Len, Mid, Replace, InStr, etc.</title><meta name="description" content="The following functions and procedures can be used to manipulate general strings, and more or less do whatever you like with them!
If you get stuck, look at the bottom of this tutorial for contact information."><LINK REL=StyleSheet HREF="http://transformers.org.uk/~thecleaner/tips.css" TYPE="text/css"></head><body><div><b>Title:</b><br>String manipulation examples in VB.NET. Equivalents of Len, Mid, Replace, InStr, UCase, Split, etc.<p><b>Description:</b><br>The following functions and procedures can be used to manipulate general strings, and more or less do whatever you like with them!
If you get stuck, look at the bottom of this tutorial for contact information.<p></p>
<!-- -->
<b>VB 6 Commands and equivalents:</b><br>
<pre>
Len = .Length
Mid = .SubString
Replace = .Replace
InStr = .IndexOf
UCase = .ToUpper
LCase = .ToLower
Split = .Split
Join = .Join
</pre>
<b>1. Getting the length of a string or variable<P></b>
This produces a messagebox containing the number of characters in textbox1. This will be in the form of a numerical value.<br>
<pre>
MsgBox(Textbox1.Text.Length)
</pre>
This code produces a messagebox saying "22" because 'strText' is 22 characters long.<br>
<pre>
Dim StrText As String
Dim r As Integer
StrText = "How long is this text?"
r = StrText.Length
MsgBox(r)
</pre>
<b>2. The following code is used to get a part of a string. Useful for cutting off bits that aren't needed throughout the rest of the code. It is called the SubString function. It accepts the start position, and the number of characters you wish to read from the start position.</b><p>
The value of 'r' below will be 'to the world' because we are cutting off the first 8 characters. We have specified no number of characters to read, so 'r' will read from the 9th character to the end.
<pre>
Dim r As String = "Welcome to the world"
r = r.Substring(8)
MsgBox(r)
</pre>
In the example below, we make the read length 6. Now, the value of 'r' be be 'to the', because we start reading at 8 characters into the string, and stop reading 8 + 6 characters into the string.
<pre>
Dim r As String = "Welcome to the world"
r = r.SubString(8, 6)
MsgBox(r)
</pre>
<b>3. If you wish to search the text for a particular word, then you will use the IndexOf(Find word, StartPosition) function. This function is very customisable to your needs, and so has a lot of optional extras that can be added, but in the interests of simplicity, I'll leave these off the tutorial. The IndexOf command returns its value as an integer (number) as a place where it found the string in the search text.<P></b>
This code starts at the beginning of 'The weather today is reasonably warm and sunny', because we didn't give a start position, and searches for the word 'warm' in it. If it does not find the word warm in the string, then it will return the value as 0, and you get a message saying '0'. However, if it finds the word, then it returns a number saying where it found the start of the word. In this case, you would see a messagebox saying '32' because the 'w' of warm is 32 characters into the string.
<pre>
Dim r As String = "The weather today is reasonably warm and sunny"
r = r.IndexOf("warm")
MsgBox(r)
</pre>
If you wish to make a simple search program, to find searchword TextBox2.Text in the string TextBox1.Text, then this is how you would go about doing it:
<pre>
Dim r As Integer
TextBox1.Text = "Welcome to the grand parade"
TextBox2.text = "grand"
r = TextBox1.Text.IndexOf(TextBox2.Text)
 If r > 0 Then
  MsgBox("Found word, " & r & " characters into the search string.")
 Else
  MsgBox("Sorry, could not find the search text")
 End If
</pre>
If the above code works correctly (and it should :) then you should get a message box telling you the word was found 15 chars into the search string.<P>
<b>4. Next, is .Replace(search for text, replace with text). It is used to search through a string, and replace certain words or characters with other ones. The Replace function returns the text that it has replaced.<P></b>
This code would produce a message replacing the word 'fool' with 'brave bloke', and therefore will look like this: 'Only a brave bloke goes <br>outside in the cold without a coat on'.
<pre>
Dim i As String = "Only a fool goes outside in the cold without a coat on"
i = i.Replace("fool", "brave bloke")
MsgBox(i)
</pre>
Another example of this use, is to remove a swearword from a sentence etc, as follows: This code searches through TextBox1.text, and replaces all instances of 'oh my god', with 'oh my goodness', then returns the text back into TextBox1.text, without the cursing.
<pre>
TextBox1.Text = "I was walking through the park when I realised I was insane. 'oh my god', i said out loud"
TextBox1.Text = TextBox1.Text.Replace("oh my god", "oh my goodness")
</pre>
To define the point where the Replace function starts searching the string, include the number of characters you wish to start from in the command. Not only does this example only replace the second 'e' with an 'E', it cuts off the string from the point you specify. The outcome of the line above would be 'TEst'.
<pre>
MsgBox(Replace("Test Test", "e", "E", 6))
</pre>
<b>5. Converting a string to uppercase / lowercase<P></b>
This is useful for making sure that if a user types something in uppercase (capitals) then it will still comply with something in your code that is lowercase. For example, if you are making a text adventure, and the user is given a choice of left or right, and they type LEFT, as VB is case sensitive, your program wouldn't accept their answer, and tell them it was invalid! To combat this, you use the string.ToUpper or string.ToLower commands<P>
To make a sentence uppercase, you use the following:<br>
<pre>
Dim r as String
r = "Isn't the internet FABULOUS!"
r = r.ToUpper
TextBox1.Text = r
</pre>
TextBox1 will now contain the words 'ISN'T THE INTERNET FABULOUS!'<br>
Or to convert to lowercase, use the following:
<pre>
Dim r as String
r = "Isn't the internet FABULOUS!"
r = r.ToLower
TextBox1.Text = r
</pre>
TextBox1 will now contain the words 'isn't the internet fabulous'<P>
<b>6. Reversing the order of characters in a string.<P></b>
If you wish to flip around the front and back end of a string, then the StrReverse(string) is for you. It is used in the following way. This would pop up a message saying 'esabatad egral rehtar a si CSP'. I'm not quite sure why you'd want to use this function, but may be useful to know!<br>
<pre>
MsgBox(StrReverse("PSC is a rather large database"))</font><br>
</pre>
<b>7. Comparing strings in terms of ASCII values / Case.<P></b>
The String.Compare function seems reasonably useful in this field. It is used in context String.Compare(string1, string2). This function returns its value as an integer, specifying what it found. In this case, you would get TextBox1.Text giving you the value 1, because tHe_cLeanER is greater in ASCII value than THE_CLEANER.
<pre>
TextBox1.Text = String.Compare("tHe_cLeanER", "THE_CLEANER")
If TextBox1.Text = -1 Then
 MsgBox("String 1 is less than string 2")
End If
If TextBox1.Text = 0 Then
 MsgBox("String 2 is equal to string 1")
End If
If TextBox1.Text = 1 Then
 MsgBox("String 1 is greater than string 2")
End If
If TextBox1.Text = "" Then
 MsgBox("String 1 and / or string two is null")
End If
</pre>
<b>8. Creating arrays with the Split(split-character) function.<P></b>
This function allows you to create a one-dimensional array, by splitting a string by
recognizing a certain character, then putting any text after the character on a new line in the array.<br>
This code will pop up a message box For each item in the array, which is 4. Note that the first line is infact 0.
<pre>
Dim i As String = "Line 0|Line 1|Line 2|Line 3"
Dim a() As String
Dim j As Integer
a = i.Split("|")
For j = 0 To a.GetUpperBound(0)
 MsgBox(a(j))
Next
</pre>
Another use of this function could be for getting all the lines from a multiline text box as follows: This will pull all lines of the text box, and use them to create an array, which is stored in r. You extract these values from the array by selecting where in the array you wish to look. The look-in-line is defined after the r, in brackets. Example: Msgbox r(3) would pull the FORTH line of the array that is being held in r. Msgbox r(5) would pull the 6th line being held in the array.<br>
<pre>
Dim a() As String
Dim j As Integer
a = TextBox1.Text.Split(Lf)
For j = 0 To a.GetUpperBound(0)
 MsgBox(a(j))
Next
</pre>
<b>9. Joining an array back into one string. Uses the .Join(split character, array) function.<P></b>
If you have an array, and wish to compile it back into one string, then the Join function (Which is the opposite of the Split function) is the one to use. This code will put back together an array into a string, separating different lines in the array with the specified character. In this case, I used the carriage return char, which is the equivalent of pressing Enter. The above code will compile an array created from a multiline text box. It will work fine with the previous procedure.
<br>
Note: this will only work if 'a' contains an array. See previous to create an array.<br>
<pre>
Dim r As String
Dim a() As String
r = String.Join(vbCrLf, a)
MsgBox(r)
</pre>
<font size ="-1"><b>Submitted by: tHe_cLeanER</b>
<br>Thanks to <a href="http://www.avenuezx.com/vbnet4apps/">VBnet4Apps</a> for code formatting and CSS.
<br>E-mail: <a href="mailto:jBistoGOOD@Hotmail.com">Contributor</a></div></font></body></html>

