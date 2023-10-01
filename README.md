Spring Boot 3.1.4

A Simple Spring Boot Email integration to register, otp verification, re generation and login apis

Go to gmail account and generate password 
Login to Gmail 
    -> Manage your Google Account 
        -> Security 
            -> App Passwords 
                -> Provide your login password 
                    -> Select app with a custom name (ex: springbootemail)
                        -> Click on Generate
                        
                        
Paste this password in application properties file

http://localhost:8080/register
POST
{
    "email": "xyzemail@gmail.com",
    "name": "AnyName",
    "password": "DSR1234"
}                   


http://localhost:8080/verify-account?email=srss.rajesh@gmail.com&otp=908908

Generate new OTP afte
http://localhost:8080/verify-account?email=srss.rajesh@gmail.com&otp=111111

ReGenerate OTP
http://localhost:8080/regenerate-otp?email=srss.rajesh@gmail.com

After verification
http://localhost:8080/login
{
    "email": "xyzemail@gmail.com",
    "password": "DSR1234"
} 

     
