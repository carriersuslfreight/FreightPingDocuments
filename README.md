# USL Freight Ping

The user of this application will install the app from either the Apple App Store or Google Play
Store.  On initial startup will enter a valid phone number with area code, and click a call to
action button.  This action will start a background service that will retrieve the users GPS
latitude and longitude and send it to a server.  This location update will continue if the
application is backgrounded.

##Requirement Notes

###Initial Startup:
- The application will make a request to the web server to get the reporting interval time
    - The response will be in XML format and indicate number of minutes
    - If the connection cannot be made, and error dialog is shown


###Phone Number Field:
- User will enter phone number once on startup, but have option to change the number later.
- Field will accept only digits, with no extra characters such as ( ) or -
- Field will be validated for containing 10 digits
- ? If user enters < 10 digits, an error dialog box is shown
- The phone number will be saved to preferences and shown to the user on subsequent startups.

###Screen orientation:
- ? Orientation locked to Portrait

###CTA Button:
- The initial state of the button will be in an OFF button style with a title of “Start Tracking”
- When the user clicks the button, the title will change to “Stop Tracking” with an ON button style
    - The phone number field clears and the number is saved to preferences
- When the user clicks the button to stop tracking, the button title changes and the phone number saved to preferences populates the phone number field

###Location Reporting:
- The app will report location using the retrieved reporting interval.
- The app will report location when the app is backgrounded
- The app will not report location when the app is not in a running state.
- ? If the app cannot report location, an error dialog will be displayed to user, message depending on error condition:
    - No network or GPS available
    - Web service down


