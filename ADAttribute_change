cls
$name = "username"
$ID = "0815"
$department = "XX"
$title = "Testuser"
$location = "Ort"
$telefon = "+49 911 123 456 789"
$email = "name@e-mail.de"
$UserOU = "Abteilung"



Get-ADUser $name -Properties msds-cloudextensionattribute20,employeeID,department,title,l,manager,mail,telephonenumber
pause
Set-ADUser $name -add @{"l"="$location"}
Set-ADUser $name -add @{"msDS-cloudExtensionAttribute20"="$UserOU"} -employeeID $ID -department $department -title $title -manager $manager
Get-ADUser $name -Properties employeeID,msds-cloudextensionattribute20,department,title,l,manager,mail,telephonenumber

#Set-ADUser $name -telephonenumber $telefon
#Set-ADUser $name -mail $email
#Get-ADUser $name -Properties employeeID,msds-cloudextensionattribute20,department,title,l,manager,mail,telephonenumber
