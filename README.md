## Running-batch-jobs-D365
- Sample code for the implementation of a batch job that cleans up old data in Dynamics 365 Finance and Operations using the Service, Contract, and Controller classes, 

- In this example, the Service class contains the actual data cleanup logic, the Contract class defines the input parameter for the batch job (in this case, the cutoff date for the data cleanup), and the Controller class handles the user interface for the batch job and calls the Service class to perform the cleanup.

- Note that the Controller class extends the RunBaseBatchController class, which is the standard base class for batch job controllers in Dynamics 365 Finance and Operations. The Controller class also implements the pack() and unpack() methods, which are used to pack and unpack the Contract class data.

- To create the batch job in the AOT, you would create a new batch job and set the class property to the Controller class ("DataCleanupBatchJobController" in this example). In the Parameters node of the batch job, you would add a parameter for the cutoff date, which corresponds to the "cutoffDate" property in the Contract class. You can then schedule the batch job to run at the desired frequency using the Batch Job Scheduler.
