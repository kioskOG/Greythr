# Greythr Automated Sign-In/Sign-Out Script

This Python script automates the sign-in and sign-out process on a website using Selenium. It schedules the sign-in and sign-out tasks from Monday to Friday at random times within a specified range. Additionally, it captures screenshots and sends email notifications upon successful execution.

## Features
- ✅ Automated sign-in/sign-out using Selenium.
- ✅ Uses headless Chrome browser for automation.
- ✅ Sends email notifications for successful actions.
- ✅ Takes a screenshot of the process.
- ✅ Uses a scheduler to run tasks on weekdays.
- ✅ Secure credential management via YAML configuration.

---
## Installation & Setup

### Prerequisites
Ensure you have the following installed on your system:
- Python 3.x
- Google Chrome
- Chrome WebDriver
- Required Python packages

### Install Dependencies
Run the following command to install required Python packages:
```bash
pip install selenium webdriver-manager pyyaml schedule pytz random datetime time yaml smtplib logging os
```

### Configure Credentials
Create a file named `h-input.yaml` in the same directory and add the following details:
```yaml
website_link: "<WEBSITE URL>"
username: "<YOUR USERNAME>"
password: "<YOUR PASSWORD>"
email_sender: "<YOUR EMAIL>"
email_password: "<YOUR EMAIL PASSWORD>" # Use Google App Passwords  https://myaccount.google.com/u/1/apppasswords
email_host: "smtp.gmail.com"
email_port: 587

email_recipients:
  - name: "Recipient One"
    email: "<RECIPIENT EMAIL>"
```

### Running the Script
Run the script using:
```bash
python main.py
```
The script will schedule sign-in and sign-out actions from Monday to Friday at random times.

---
## How It Works
1. **Loads Credentials:** Reads credentials from `h-input.yaml`.
2. **Connects to Website:** Uses Selenium to log in.
3. **Executes Sign-In/Sign-Out:** Clicks appropriate buttons on the website.
4. **Captures Screenshot:** Saves a screenshot for verification.
5. **Sends Email Notifications:** Notifies users of successful execution.
6. **Schedules Tasks:** Runs tasks at randomized times within a given range.

---
## Debugging & Logs
If the script encounters errors:
- Check the console logs for error messages.
- Ensure ChromeDriver is installed and accessible.
- Validate `h-input.yaml` for correct credentials.
- Try running the script with UI by removing `--headless` from `webdriver` options.

---
## Contributing
Feel free to modify and enhance the script. Contributions are welcome!
