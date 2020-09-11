# GeckoDriver-Example

What is Gecko Driver?
The term Gecko stands for a Web Browser engine that is inbuilt within Mozilla Firefox browser. Gecko driver acts as a proxy between Web Driver enabled clients(Eclipse, Netbeans, etc.) and Mozilla Firefox browser. In short, Gecko driver acts as a link between Selenium Web Driver tests and Mozilla Firefox browser.

Before Selenium 3, Mozilla Firefox browser was the default browser for Selenium. After Selenium 3, testers need to initialize the script to use Firefox using GeckoDriver explicitly. Selenium uses W3C Webdriver protocol to send requests to GeckoDriver, which translates them into a protocol named Marionette. Firefox will understand the commands transmitted in the form of Marionette protocol and executes them.

Advantage of using Gecko Driver
Selenium Webdriver version 2.53 is not compatible with Mozilla Firefox version 47.0+. The Firefox driver used in earlier versions of Mozilla Firefox will be discontinued, and only the GeckoDriver implementation would be used. Hence testers are forced to use GeckoDriver if they want to run automated tests on Mozilla Firefox version 47.0+. But the big question - what is the advantage?
The major advantage of using GeckoDriver as opposed to the default Firefox driver is Compatibility. GeckoDriver uses W3C WebDriver protocol to communicate with Selenium. W3C is a universally defined standard for Web Driver. This means Selenium Developers (People who code Selenium base) need not create a new version of Web Driver for each browser version. The same Web Driver can be used for multiple browser versions. Hence, GeckoDriver is preferred compared to the earlier implementation of Firefox driver.

 At this page https://github.com/mozilla/geckodriver/releases ,Select the appropriate version for GeckoDriver download based on your operating system
 
 
