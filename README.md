Golang CLI Reminder
This is a simple command-line tool written in Go that allows users to set reminders for future times. The tool will notify the user via a desktop notification at the specified time.

Features
Set a reminder by specifying a time and message.
Sends a desktop notification when the time is reached.
Supports natural language time parsing (e.g., "9:12").
Can be run directly from the terminal.
Prerequisites
Before using this project, ensure that you have the following installed:

Go (1.16+)
Beeep for sending desktop notifications.
When for natural language date/time parsing.
Install Dependencies
Use go get to install the required packages:

bash
Copy code
go get github.com/gen2brain/beeep
go get github.com/olebedev/when
Usage
To use this reminder tool, run the following command:

bash
Copy code
go run main.go <time> <message>
<time>: Time in hh:mm format (24-hour format).
<message>: The reminder message to display when the time is reached.
Example
bash
Copy code
go run main.go "12:30" "Time for lunch!"
This will set a reminder for 12:30 PM, and a notification will appear at that time with the message "Time for lunch!"

Notes
The time must be a future time.
The system time should be correctly set to avoid issues with time comparisons.
Notifications will only appear when the correct time is reached.
Troubleshooting
Set a future time error: If you receive the message set a future time!, make sure the time you provided is in the future. Double-check that you're using the 24-hour time format and that your system time is correct.

Unable to parse time: Ensure that the time format is hh:mm and matches a valid 24-hour time.

License
This project is licensed under the MIT License. See the LICENSE file for more details.
