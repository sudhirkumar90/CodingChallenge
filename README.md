#Automation Framework Description:


#Components of the Framework:
1)	Selenium WebDriver
2)	TestNg
3)	Maven
4)	Apache POI
5)	Extent Report API for Reporting
6)	Java programming language
7)	Page Object Model and Object Repository


#Framework Description:
1.	This framework is using page object model to create Object Repositories for each Web-Page. 
2.	Test can be run on Chrome/ Firefox/ Safari. (tested on Chrome (53.0.2785.143), Firefox (47.0.1) and Safari (10.0.1)).
3.	All the page elements and page related functions are inside com.zendesk.objectRepository package.
4.	Test scripts (TestNg test functions) are inside com.zendesk.testcases package.
5.	com.zendesk.generic package contains all the generic functions/setup/utility files which are common to all scripts
6.	Config.properties file inside com.zendesk.config is for initial test configuration.
7.	All scripts are data driven using excel with the help of Apache POI & TestNg. The test data file location is: zendesk/TestData/TestData.xlsx
8.	Reports are generated using Extent API. Each step during the test execution is logged into the reports. verification/assertion/exception as logged along with the screenshots. The default location of the report is: zendesk/ExtendReport/<Report_Name>.html
9.	TestNg.xml is configured to run from POM.xml using maven’s surefire plugin and these scripts can be integrated with any CI tool like Jenkins.
10.	 TestData folder inside the project contains the TestData.xlsx and contains the test-data for the scripts.
11.	 ExtendReport folder inside the project contains the report and the screenshots.
12.	 Resources folder contains the browser drivers.
13.	 Framework is developed using modular programming.


#How to execute:
1.	Unzip zendesk.zip
2.	Import the zendesk folder as maven project into Eclipse.
3.	Right click and maven->update project. 
4.	Open Config.properties file and make the initial configurations changes. For e.g. Browser, ReportName, etc.
5.	Ways to start the execution:
    a.	Run the TestNg.xml file using TestNg.
    b.	Run the TodosTC.java class from com.zendesk.testcases using TestNg.
    c.	Right click and maven-test on Pom.xml


