# M133-Project - everone

# Introduction

We have created a group of 4 members in class BI17b. Among them are the following team members: 
Francesco De Nuccio, Drilon Krasniqi, Alessio Benintende and Alexander Schwerzmann. 
With this grouping we can divide the tasks very well and are making good progress. 
As we have already proven our cooperation in various projects and this has always been positive.

Our goal is that we create a website where you can log in and
then use our tool. We would like to create an online note platform, where
every user can take notes.

Our preparation consists of creating a GitHub repository, all
team members and then upload the documents for our
Deposit website.

The tasks were split like this:
Create a design: All of us
Pick out the hoster: Krasniqi Drilon
Execute the design and create the web pages: Benintende Alessio, Schwerzmann Alexander
PHP,functionality, database connection: De Nuccio Francesco Krasniqi Drilon

# Documentation
## Archtecture
Our web page is simply built and consists of three layers:
Presentation layer that includes HTML and CSS.
Backend layer that includes PHP.
Data layer where we used a MySQL database.

## Technology
As previously mentioned we are using PHP which is easy to use and learn.
There have been many web pages that have used PHP.. However, it is slowly dying out and being replaced by C#, Javascript, Python etc.
One of the other reasons why we used PHP is that the teacher is familiar with the technology and could help us, if there was any need of it.

## Application design
### Flow
As you type in http://everone.me you will be redirected to our main page, index.php.
From there on you can choose between "Register" or "Login".
#### Registration
On the "Register" page you can create an account with information such as your username, e-mail and password. This will send your data to our database.
We want that the username and e-mail to be unique, therefor if you enter an already existing user, it will warn you and not let you create a user. This check is done in our database.

![alt text](https://github.com/fdenuccio/M133-everone/blob/master/images/username_already_in_use.png "Username is already in use")

![alt text](https://github.com/fdenuccio/M133-everone/blob/master/images/email_already_in_use.png "E-Mail is already in use")

If your repeated password doesn't match you first password, it will also give you a warning. 

![alt text](https://github.com/fdenuccio/M133-everone/blob/master/images/password_dont_match.png "Passwords do not match")

However, if everything is fine, the e-mail and username are unique and the passwords match, it will create an entry in our database. For additional security the chosen password by the user is  getting hashed and then being added.

#### Login
If you already have a user, you can log in with your e-mail and your chosen password.
The hash value of the password gets created before getting sent to the database. There the two hash values get compared, if they match you will be granted access to your account.
If the e-mail and the password don't match, it will tell you, that the credentials are invalid.

![alt text](https://github.com/fdenuccio/M133-everone/blob/master/images/invalid_credentials.png "Invalid credentials")

## Application Structure
Our application structure was very easily built. 

**css** All our design layouts are here saved in this folder.
**html** The very few HTML sites that we had, are in this folder.
**images** All the images used for our page are located here.
**js** If we had needed any javascript files, they would've gone in here. However for now it was just a placeholder.
**php** This is the most important folder with all our PHP pages.
**First layer** On here is our index page.

![alt text](https://github.com/fdenuccio/M133-everone/blob/master/images/application_structure.png "Application Structre")

# GUI

First we created a mockup for our webpage to have some kind of idea how it should look.
![alt text](https://github.com/fdenuccio/M133-everone/blob/master/images/mockup.png "Mockup Everone")

With this mockup it was easy for us to get the final design of our webpage. 

**Login Page**
![alt text](https://github.com/fdenuccio/M133-everone/blob/master/images/login.png "Login Page")

**Register Page**
![alt text](https://github.com/fdenuccio/M133-everone/blob/master/images/register.png "Register Page")

# Test Cases

| Test Case    | C01 False data input in register and login form.                                                                              |
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| Goal         | The input is being tested of existing data or wrong passwords.                                                                |
| Input        | Username: M133 (already in database) <br/> E-Mail: m133@everone.me (already in the database) <br/> Password: M133.TBZ Repated: M122.TBZ | 
| Shall-Value  | E-Mail is already in use. Username is already in use. Passwords do not match.                                                 |
| Is-Value     | ![alt text](https://github.com/fdenuccio/M133-everone/blob/master/images/username_already_in_use.png "Username is already in use") <br/> ![alt text](https://github.com/fdenuccio/M133-everone/blob/master/images/email_already_in_use.png "E-Mail is already in use") <br/> ![alt text](https://github.com/fdenuccio/M133-everone/blob/master/images/password_dont_match.png "Passwords do not match") |

| Test Case    | C02 Wrong password when logging in.                                                                              |
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| Goal         | The user won't be able to log in.                                                                 |
| Input        | Username: M133 <br/> Password: M122.TBZ <br/> Actual Password: M133.TBZ | 
| Shall-Value  | Invalid Credentials.                                                 |
| Is-Value     | ![alt text](https://github.com/fdenuccio/M133-everone/blob/master/images/invalid_credentials.png "Invalid credentials") |

| Test Case    | C02 Wrong password when logging in.                                                                              |
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| Goal         | The user won't be able to log in.                                                                 |
| Input        | Username: M133 <br/> Password: M122.TBZ <br/> Actual Password: M133.TBZ | 
| Shall-Value  | Invalid Credentials.                                                 |
| Is-Value     | ![alt text](https://github.com/fdenuccio/M133-everone/blob/master/images/invalid_credentials.png "Invalid credentials") |

| Test Case    | C03 Session handeling.                                                                              |
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| Goal         | When logged in, cookies will be created.                                                                 |
| Input        | Username: M133 <br/> Password: M133.TBZ | 
| Shall-Value  | user_id, username, email, PHPSESSID                                                 |
| Is-Value     | ![alt text](https://github.com/fdenuccio/M133-everone/blob/master/images/session_test_case.png "Session Cookies") |

# Reflection

## Alessio Benintende:
Dieses Modul war eine gute Gelegenheit, um HTML und PHP wiederaufzufrischen.
Es war eine neue und spannende Erfahrung das Modul ??ber Homeschooling durchzuf??hren.
Im grossem ganzen war es ganz gem??tlich zuhause zu arbeiten, doch das Problem dabei ist, dass man mehr Ablenkung als sonst hat und sich nicht immer gut konzentrieren kann.
Schlussendlich fand ich das Modul ganz in Ordnung und die Team Arbeit machte mir Spass.

## Drilon Krasniqi:
Das Modul war im Grossen und Ganzen zufriedenstellend. Doch die Anfangsaufgaben fand ich pers??nlich nicht so n??tig und sie h??tten mit der Projektarbeit ersetzt werden k??nnen. Wir haben damit sehr viel Zeit investiert und hatten somit weniger Zeit f??r das Projekt selber. Am Schluss bekamen wir ein bisschen Stress das Projekt noch fertig zu stellen. Das allerbeste fand ich von Zuhause aus arbeiten zu k??nnen. Denn ich kann viel l??nger schlafen als sonst und auch fr??her Feierabend haben als sonst und die Motivation ist daher gr??sser. Ich fand wir waren produktiver Zuhause als in der Schule, da man weniger Pausen etc. macht und nicht andere Mitsch??ler die einem Ablenken um sich hat. Die Team Arbeit machte mir Spass und durch das Modul konnte ich alles nochmals neu auffrischen.

## Francesco DeNuccio

In diesem Modul hatte ich von unserem Team die meiste Erfahrung, aus diesem Grund haben wir uns dazu entschieden, dass ich den Lead ??bernehme. Damit ich immer allen von unserem Team alles erkl??ren konnte, was wie funktioniert etc. war es in der Schule optimal. Auch wenn es zu einzelaufgaben kam konnte ich die meistens verst??ndlich f??r die anderen erkl??ren. Das habe ich bemerkt, da sie mir das als R??ckmeldung gaben und das Projekt auch weiter vorankam.

Als wir wegen COVID-19 im Distance-Learning waren, konnte ich die Erkl??rungen nicht mehr ganz so gut t??tigen. Aus diesem Grund fingen wir an ein bisschen hinterher zu sein und gegen Ende hat dies uns unter Druck gesetzt.

F??r eine gute Benotung, war es eine Anforderung das Session-Handling zu haben. Ich habe mich bem??ht dieses funktionst??chtig aufzubauen. Dies war sehr schwer und da ich Stress ausgesetzt war, hatte ich eine schlechtere Konzentration. Aber mit starkem durchhalte Wille konnte ich einen fortschritt bewirken.

Ich fand das Modul sehr interessant.

Die Anfangsaufgaben waren zu einfach und haben zu viel Zeit in Anspruch genommen.

Die Theorieinputs waren zum Grossteil zu lang. Wir haben die meisten Inputs bis zum Sessionhandling bereits in anderen Modulen besprochen.

Das Distance-Learning hat mir Spass gemacht, ich finde es besser als normale Schule. Ich bin viel konzentrierter als sonst.

## Alexander Schwerzmann

Ich fand das Modul im Prinzip gut. Es war jedoch sehr schwer und ich denke nicht dass es f??r jede Person einfach war. Ich hatte das Gl??ck und hatte Teamkollegen welche mir alles erkl??ren konnten.

Die Anfangsaufgaben waren f??r mich gut. Jedoch waren die ersten Aufgaben dann auch wieder einfach f??r mich.

Die Theorieinputs waren zum meistenteil sehr gut und wenn man aufgepasst hat konnte man viel mitnehmen. Ich w??rde es hilfreich finden wenn es noch Theoriebl??tter/Merkbl??tter g??be.

Das Distance-Learning hatte mich positiv beeinflusst und ich konnte besser Arbeiten.



# Learnings Krasniqi Drilon

## **10.03.2020**
Zu Beginn haben wir zusammen eine Skizze dargestellt, auf der wir umgef??hr sehen k??nnen, wie unsere Webpage wird. Dadurch wussten wir dann, wie die Applikationsstruktur aussehen wird und wir erstellten ein Projekt auf Github. Dadurch konnten wir alle gemeinsam darauf arbeiten.

## **17.03.2020**
Schulausfall wegen Corona.

## **24.03.2020**
Heute haben ich versucht einen Hoster f??r unsere Webpage herauszusuchen. Ich hate bplace und InfinityFree zur Auswahl und ich habe mich f??r InfinityFree entschieden. Es hat mehrere positive Bewertungen als die beste Free Hosting Variante. Ich habe danach mich eingelesen und herausgefunden was man alles darauf machen kann.

## **31.03.2020**
Nachdem ich verstanden habe wie unser Hoster funktioniert, haben Herr DeNuccio und ich uns an die Datenbankanbindung gemacht. Es gab vorerst ein Paar Komplikationen, da man die SQL Datenbank mit speziellen Anmeldeinformationen erreichen kann. Dies konnten wir aber beheben und die Tabellen etc. wurden von mir ??ber das Webinterface gemacht.

## **07.04.2020**
Heute haben ich meistens am Layout der Webpage gearbeitet und so das Aussehen ein bisschen ver??ndert und angepasst.

## **28.04.2020**
Unser Hoster war nicht erreichbar heute und die Seite hat nicht richtig geladen. Ich habe mir das angeschaut und beheben k??nnen. Zudem hatten wir festgestellt, dass die falschen Files hochgeladen wurden. Dies konnte auch korrigiert werden. Die Seite lief dann wieder normal und war erreichbar.

## **05.05.2020**
Heute war der letzte Tag des Projektes. Wir haben noch die letzten Arbeiten gemacht und ich habe die Dokumentation fertiggeschrieben. Session-handeling war das letzte, was wir noch machen mussten. Dies hat dann nun funktioniert.

# Learnings Benintende Alessio

## **10.03.2020**

Am ersten Tag haben wir die Gruppen gebildet. Ich bin sehr zufrieden mit meiner Gruppe, ausser dass wir eine Person zu viel sind. Aber trotzdem habe ich nichts dagegen. Es wird dann einfach so sein, dass einer nicht richtig etwas zu tun hat. Nat??rlich wurde ich in meiner Gruppe als Teamleiter erw??hlt. Ich finde dies sehr weise entschieden von den andern, da ich in meinem Gesch??ft selbst schon Erfahrungen damit gesammelt habe und daher sehr gut ein Team leiten kann. Den Rest des Tages bekamen wir Inputs und einen Einstieg zum Modul. 

 
## **17.03.2020**

Heute war keine Schule wegen Corona. 

## **24.03.2020**

Heute haben wir zuerst ein paar Inputs bekommen. Ich habe ein paar neue Dinge durch die Inputs gelernt, die m??glicherweise sp??ter wichtig werden. Danach habe ich mich mit meinem Team zusammengesetzt. Heute was die Aufgabe unser Projekt zu bestimmen. Ich habe zuerst versucht ein altes Projekt wieder zum Leben zu erwecken, da wir mit dem vieles bereits abdecken h??tten k??nnen, doch leider habe ich dies nicht geschafft und wollte keine Zeit mehr daf??r verschwenden. Also haben wir uns m??gliche Projekte ??berlegt, womit wir alle Kompetenzen abgleichen k??nnen. Als wir unser Projekt entschieden haben, war der Tag auch bereits fertig. 

 
## **31.03.2020**

Heute bekamen wir wieder ein paar Inputs. Auch dieses Mal haben wir wieder ein paar wichtige Sachen gelernt. Heute haben wir mit unserem Projekt angefangen. Wir haben die komplette Struktur aufgebaut und aufgezeichnet und noch mit der Dokumentation begonnen. 

 

## **07.04.2020**

Heute haben wir an unserer Index Seite gearbeitet. Wir haben unser Design erstellt und haben bereits mit dem Cod angefangen. Auch heute bekamen wir ein paar Inputs, die sehr wichtig waren. 


## **28.04.2020**

Heute haben wir unsere Login Seite fertiggestellt. Wir haben mit php und MySQL gearbeitet. Heute habe ich eine index Website fertiggestellt. Zus??tzlich habe ich noch das Registrieren hinzugef??gt. 

## **05.05.2020**

Heute haben wir alles fertiggestellt und noch verbessert. Was noch nicht richtig funktioniert hat, haben wir noch korrigiert. Learnings dokumentiert. 



