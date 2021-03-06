This little script runs in the Google App Script environment.

Specifically it runs in [Google Spreadsheets][0]. It lets you suck down your Fitbit data and the do all kinds of analysis.  It's also an easy way to get started with the Fitbit API. This code is based on the work loghound did in [his project][3]. I have added support for heart rate figures that are produced by a Fitbit Charge HR. This version can also be scheduled using triggers.

If you want to know how OAuth 2.0 works, have a look at [a sample][2].

Sadly to get started is a bit of a pain:

1. Create a new Google Spreadsheet.
2. Go to Tools-->Script Editor
3. Replace the template with fitbit.js.
4. Save your changes and reload your sheet. 
5. From the Fitbit menu in your Spreadsheet, run the Configure option. If you don't see the option, run "onInstall" function in script editor and try again.
6. Follow the instructions given in the form that pops up. You'll have to set up a Fitbit dev account.
7. Run the "Authorize" menu option -- this will run through the OAuth dance.
8. Run the 'Refresh fitbit Time Data" menu option to get your data
9. Profit!

Optional:
10. Set up a trigger for your script to run periodically.
	- Script editor --> Resources --> All your triggers --> Add a new trigger for "refreshTimeSeries".

[0]: http://drive.google.com
[1]: https://github.com/loghound/Fitbit-for-Google-App-Script
[2]: https://github.com/googlesamples/apps-script-oauth2
[3]: https://github.com/loghound/Fitbit-for-Google-App-Script