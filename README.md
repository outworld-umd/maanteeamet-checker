# Maanteeamet Driving Exam Time Checker
This application was built by me and for me with a sole purpose to get earlier driving exam time in Maanteeamet (Estonian Road Administration).
This program managed to find me an exam time in 4 days (which I then failed), and then the new one in 3 days.

***Important!** Since September 2020, you no longer need to login to Maanteeamet's self-service in order to check the free exam times, as the data is now accessible [here](https://eteenindus.mnt.ee/public/vabadSoidueksamiajad.xhtml).
However, there have been some talks that aforementioned page does not always have the up-to-date information, i.e. some free exam times are not shown.*

## About
It works as follows:
1. Insert the necessary information into the ```main.properties``` (described below)
2. Run the application and login with Smart-ID when the page asks you to
3. Wait for the exam time to appear by checking your emails constantly
4. Once you've got email, take the free time

### How to use

Firstly, you need Java 14 on your computer. Once you've got that installed, fill the ```main.properties``` with the information:
```
MAIL_ADDRESS=some-address@gmail.com   # used ONLY for sending the emails to yourself
PASSWORD=sUpErSeCrEtPaSsWoRd          # if using Gmail, app token can be acquired here: https://myaccount.google.com/apppasswords
EXAM=01.01.2100 10:15                 # current exam time in format DD.MM.YYYY HH:mm
ID_CODE=37001010xxx                   # Estonian ID-code used for automated login
TIMEOUT=8                             # time between the next checks (seconds)
```
Just run the application and wait.

All the check results are being saved to a file ```log.txt``` (example of logging is in ```log-example.txt```).

### Program is built using
- Java 14
- Selenium Web Driver
- Maven

## Testimonials

_"Very good app, helped me find a free exam time tremendously fast!"_  —  me

_"Agree with the comment above!"_  —  also me

_"Yeah, it really works, and is indeed pretty useful!"_  —  some of my buddies

## Version history
- **0.2.0** *(latest)* - Add simple GUI, fix bugs
- **0.1.2** - Add possibility to choose the timeout
- **0.1.1** - Fix the gap in logic
- **0.1.0** - Switch the authentication method from ID-card to Smart-ID
- **0.0.2** - Move the email data changing to properties file
- **0.0.1** - Initial version of the checker
