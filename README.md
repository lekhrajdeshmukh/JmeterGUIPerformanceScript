This performance test script consist of the below components:
-------------------------------------------------------------
-------------------------------------------------------------

1) User defined variable: This test steps used to contains configuration in key-value format.
2) CSV Data set config: This test step contains the input data in csv format and also we have option to define input field name
3) Module controller: This test step contains the execution of specific test components i.e. test fragment
4) Test Fragment: This test step cotains one or more test steps
5) If controller: This test steps is used to perform conditional check
6) BeanShell sampler: This test step is used for implementing the check which is not available out of the box inside Jmeter
7) Uniform random timer: This test step is used for implement the constant wait while execution of test steps
8) Regular expression extractor: This step is used for extracting the dynamic value which used on further steps


Execution of jmeter script:
-------------------------------
* Pre-requisite:
    - Jmeter
    - Java

* Steps to execute test script
  - Download or pull the test scritp from github
  - Update your email and password details on TestData.csv
  - execute the test script from command line
    *  Open command prompt or terminal on your respective operating system
    *  Change the directory to apache Jmeter bin folder(If path is not configured on PATH(in windows) or in .bash_profile (On Linux) )    i.e.  "cd <path/to/apache/bin/folder>"
    *  Enter below command to execute and generate the csv file and default jmeter report
        * jmeter -n -t SeleniumDemoStore-II_WhenProductAvailable_Parameterization.jmx -l TestResult/SeleniumDemoStore.jtl -e -o  TestResult/SeleniumDemoStoreResult/
        
        * Where
            * -n : This switch indicates to execute test script in non-gui mode
            * -t : This switch indicated the name of the test script which used for execution
            * -l : This switch used to generate the result file in the jtl or csv format(Please pass absoulte path if you want to generate file to different folder otherwise it will create inside current path)
            * -e : This switch used for extracting the test result
            * -o : This switch indicates the folder location where default jmeter test result will get created(Please pass absoulte path if you want to generate file to different folder otherwise it will create inside current path)
            
* Note:
    * Directory "TestResult" should be present on the current directory
    * These is possiblity that product would not be available in the website, so configure testData.csv file with the product available on the site.
    * If product is not available then you will see error message "Product ["<name-of-the-product>"] is currently out of stock" on console

