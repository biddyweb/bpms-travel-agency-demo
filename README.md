JBoss BPM Suite Travel Agency Demo
==================================
This is an online employee travel booking process project. It contains multimple web services for looking up data for the process
and rules to calculate pricing. Furthermore, there are several tasks that can be activated to evaluate pricing and to review the
final booking data before completing the booking.

Welcome to the JBoss BPM Travel Agency!


Quickstart
----------
1. [Download and unzip.](https://github.com/jbossdemocentral/bpms-travel-agency-demo/archive/master.zip)

2. Add products to installs directory. For example download and add BPMS installer jar into the installs directory.

3. Run 'init.sh' or 'init.bat' file. 'init.bat' must be run with Administrative privileges.

4. Start JBoss BPMS Server by running 'standalone.sh' or 'standalone.bat' in the <path-to-project>/target/jboss-eap-6.1/bin directory.

5. Login to http://localhost:8080/business-central

  ```
  - login for admin and other roles (u:erics / p:bpmsuite1!)
  ```


Booking a trip to Edinburgh (just one scenario)
-----------------------------------------------
1. Build & deploy project.

2. Start process with following data in start form:

  ```
  Name: [your-name]

  Email Adress: [any-email]

  Number of Travellers: 2  

  From Destination: London

  To Destination: Edinburgh

  Preferred Date of Departure: 2014-12-20

  Preferred Data of Arrival: 2014-12-29

  Other Details / Notes: [any-text]
  ```

3. Login to http://localhost:8080/business-central

  ```
  - login for admin role (u:erics / p:bpmsuite1!)
  ```

4. Two web services will be run and a sub-process to calculate the cost before deciding it is not needed that this booking be
	 reviewed on pricing, so you will find a task 'Employee Booking' for you to process.

5. Navigate to the "Tasks" tab and click on it. From the task in the list, click on the "Lock" icon to claim the task

6. Click on the "Work" tab from the resulting right-side pane window that opened.

7. Fill in the form provided for the task, it allows review of all the booking data submitted, generated by services and calculated
	 by the rules. You can request a review to send it back for a pricing review or check the completed box to finish the task and
   process (isBookingConfirmed).

8. Enter credit card details (beginning with 1234...) for compensation to be triggered., Expiry details of the card (e.g. 12/12) and
	 your full name.

9. Check the logs and you will see that the process has been compensated.

10. To trigger different path for successful booking of Flights, just change the 'Credit Card details' to use any card number that does not begin with 1234....

11. For details on demoing the compensation aspects of the Travel Agency demo project, see [docs/compensation-howto/README-COMPENSATION.md](docs/compensation-howto/README-COMPENSATION.md)

Supporting Articles
-------------------
[How To Excite the Travel Industry With a BPM Story](http://www.schabell.org/2014/10/how-to-excite-travel-agencies-with-bpm-story.html)


Released versions
-----------------

See the tagged releases for the following versions of the product:

- v1.0 - JBoss BPM Suite 6.0.3 and updated travel agency demo with compensation features.

- v0.2 - moved to JBoss Demo Central, updated windows init.bat support.

- v0.1 - JBoss BPM Suite 6.0.3 and travel agency demo installed.


![Agency Process](https://github.com/jbossdemocentral/bpms-travel-agency-demo/blob/master/docs/demo-images/agency-process.png?raw=true)
![Calculate Process](https://github.com/jbossdemocentral/bpms-travel-agency-demo/blob/master/docs/demo-images/calculate-process.png?raw=true)
![Travel Process Overview](https://github.com/jbossdemocentral/bpms-travel-agency-demo/blob/master/docs/demo-images/travel-process-definition.png?raw=true)
![Started Process](https://github.com/jbossdemocentral/bpms-travel-agency-demo/blob/master/docs/demo-images/started-process.png?raw=true)
![Booking Task](https://github.com/jbossdemocentral/bpms-travel-agency-demo/blob/master/docs/demo-images/complete-booking-task.png?raw=true)
![Compensation](https://raw.githubusercontent.com/jbossdemocentral/bpms-travel-agency-demo/master/docs/demo-images/Compensation.png?raw=true)
![Special Trips UI Form](https://raw.githubusercontent.com/jbossdemocentral/bpms-travel-agency-demo/master/docs/demo-images/SpecialTripsUIform.png?raw=true)
![Special Trips UI Success Form](https://raw.githubusercontent.com/jbossdemocentral/bpms-travel-agency-demo/master/docs/demo-images/UISuccessScreen.png?raw=true)
![Task List Menu](https://raw.githubusercontent.com/jbossdemocentral/bpms-travel-agency-demo/master/docs/demo-images/TaskListMenu.png?raw=true)
![Claim Task](https://raw.githubusercontent.com/jbossdemocentral/bpms-travel-agency-demo/master/docs/demo-images/ClaimTask.png?raw=true)
![Credit Card Details](https://raw.githubusercontent.com/jbossdemocentral/bpms-travel-agency-demo/master/docs/demo-images/1234CreditCard.png?raw=true)
![Check Logs for Compensation Path](https://raw.githubusercontent.com/jbossdemocentral/bpms-travel-agency-demo/master/docs/demo-images/CheckLogsForCompensationPath.png?raw=true)
![Compensated Process](https://raw.githubusercontent.com/jbossdemocentral/bpms-travel-agency-demo/master/docs/demo-images/CompensatedProcess.png?raw=true)
![Completed Booking Process](https://github.com/jbossdemocentral/bpms-travel-agency-demo/blob/master/docs/demo-images/completed-process.png?raw=true)

