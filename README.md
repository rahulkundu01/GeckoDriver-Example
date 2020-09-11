# GeckoDriver-Example

What is Gecko Driver?
The term Gecko stands for a Web Browser engine that is inbuilt within Mozilla Firefox browser. Gecko driver acts as a proxy between Web Driver enabled clients(Eclipse, Netbeans, etc.) and Mozilla Firefox browser. In short, Gecko driver acts as a link between Selenium Web Driver tests and Mozilla Firefox browser.

Before Selenium 3, Mozilla Firefox browser was the default browser for Selenium. After Selenium 3, testers need to initialize the script to use Firefox using GeckoDriver explicitly. Selenium uses W3C Webdriver protocol to send requests to GeckoDriver, which translates them into a protocol named Marionette. Firefox will understand the commands transmitted in the form of Marionette protocol and executes them.

Advantage of using Gecko Driver
Selenium Webdriver version 2.53 is not compatible with Mozilla Firefox version 47.0+. The Firefox driver used in earlier versions of Mozilla Firefox will be discontinued, and only the GeckoDriver implementation would be used. Hence testers are forced to use GeckoDriver if they want to run automated tests on Mozilla Firefox version 47.0+. But the big question - what is the advantage?
The major advantage of using GeckoDriver as opposed to the default Firefox driver is Compatibility. GeckoDriver uses W3C WebDriver protocol to communicate with Selenium. W3C is a universally defined standard for Web Driver. This means Selenium Developers (People who code Selenium base) need not create a new version of Web Driver for each browser version. The same Web Driver can be used for multiple browser versions. Hence, GeckoDriver is preferred compared to the earlier implementation of Firefox driver.

 At this page https://github.com/mozilla/geckodriver/releases ,Select the appropriate version for GeckoDriver download based on your operating system
 
 
Common exceptions occurred while using Gecko Driver:
Following is a list of common exceptions that occur while using Gecko Driver and with resolution.

1. The path to driver executable must be set by webdriver.gecko.driver system property:

This exception occurs when user tries to instantiate Firefox driver without setting the system property for gecko driver. This is usually done by beginners to Selenium who are not aware of the changes made from Selenium 3 to Selenium previous versions.

The resolution for the above exception is to set the system property for gecko driver with the location of geckodriver.exe file as below

System.setProperty("webdriver.gecko.driver", "D:\\Downloads\\geckodriver.exe");
Please note that you need to set the property of gecko driver before creating an instance of Mozilla Firefox driver.

2. Firefox Not Connected Exception:

org.openqa.selenium.firefox.NotConnectedException: Unable to connect to host 127.0.0.1 on port 7055 after 45000 ms.
This exception usually occurs when Firefox version has been upgraded to the latest version. The resolution for this exception is to update the selenium jar file and gecko driver to the latest version and use the same.

3. Session Not Created Exception:

org.openqa.selenium.SessionNotCreatedException: Unable to create new remote session.
This exception occurs due to compatibility issues between Selenium and Gecko driver. Gecko driver works with Firefox version 47 or above. It can be resolved by updating Firefox version to 47 or above.

4. Connection Refused Exception:


WebDriver Exception: Connection Refused
This exception is the message generated when web driver is unable to establish a connection with Firefox. It can be resolved using any one of the following techniques.

Use driver.quit() method to destroy earlier instances of web driver
Clean the browser cache before executing your automated tests
Clean the project workspace within Eclipse IDE
Always use the latest version of selenium gecko driver and most recent version of Firefox browser
