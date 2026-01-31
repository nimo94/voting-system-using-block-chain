# Blockchain-Based Voting System

This web platform allows users to cast their votes securely using blockchain technology. The backend of the system is built with the Python web framework **`Django`**.

---

## How to Run

1. **Internet Connection:** Ensure your device is connected to the internet.  
2. **Install Dependencies:** Install all required Python packages using `pip`. The main dependencies are listed in `requirements.txt`.

   ```bash
   pip install -r requirements.txt
3. Configure Email:
Open Election/settings.py and locate the following variables:

EMAIL_ADDRESS = 'your_email@example.com'
EMAIL_PASSWORD = 'your_email_password'
Assign them valid credentials.

Note: See References
 for guidance.

 Development Email Handling:
To avoid hitting email API limits during development, modify the email sending code in views.py:

In send_otp() method:

[success, result] = send_email_otp(email_input)
# [success, result] = [True, '0']


In get_parties() method:

send_email_private_key(request.session['email-id'], private_key)
# print(private_key)


Run the Server:
Navigate to the directory containing manage.py and run:

python manage.py runserver


4. Access the Platform:
Open the URL shown in the terminal. By default, it is: http://127.0.0.1:8000
