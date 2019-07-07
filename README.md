This performance test script consist of the below components:
-------------------------------------------------------------
-------------------------------------------------------------

1) User defined variable: This test steps used to contains basic configuration name and it's respective value
2) CSV Data set config: This test step contains the input data in csv format and also we have option to define input field name
3) Module controller: This test step contains the execution of specific test components i.e. test fragment
4) Test Fragment: This test step cotains one or more test steps
5) If controller: This test steps is used to perform conditional check
6) BeanShell sampler: This test step is used for implementing the check which is not available out of the box inside Jmeter
7) Uniform random timer: This test step is used for implement the constant wait while execution of test steps
8) Regular expression extractor: This step is used for extracting the dynamic value which used on further steps