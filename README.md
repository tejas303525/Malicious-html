# Malicious-html
A javascript code to automatically open up desired application onto victim's machine

I am fully aware of the fact that this script can be very much used for nefariois purposes, but I did this completely for educating myself and sharing it. Please use it ***only*** to educate your mind, google the stuffs that you dont get. 

My script opens up a simple calculator but the script is completely modifyable. 

To get the base64 value of the applcation that you want to open, the following will be the syntax
```
$base64string=[convert]::ToBase64String([IO.File]::ReadAllBytes("C:\Windows\System32\calc.exe")) # change to desired appliation inside ReadAllBytes
$base64string | Out-File temperory.log #output the base64string to temperory log and open the log using some text editor and then copy it to your script
```

if your curious to see the raw content of the application before using the above code to covert to base64string, this is the syntax
```
Get-Content C:\Windows\System32\calc.exe
```
Enjoy! 
