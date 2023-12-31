🌐 Sending email alert with the help of Ansible 🌐 

Introduction: 
Ansible is such a powerful tool to send email with the help of Ansible playbook.

Requirement:

1. Ansible installed in controller node or in localhost
2. Gmail account

Tasks:

1. Go to your Google Account.
2. Select Security.
3. Under 'Signing in to Google', select 2-Step Verification.
4. At the bottom of the page, select App passwords.
5. Enter a name that helps you remember where you’ll use the app password.
6. Select Generate.
7. To enter the app password, follow the instructions on your screen. The app password is the 16-character code that is generated on your device.
8. Select Done.
9. Since the feature to send email is not included in ansible-core, this need to be downloaded from ansible-galaxy collection
10. Download the feature with below command:
ansible-galaxy collection install community.general

11. Next keep the below information handy to import in playbook:
 username i.e., the user from which id the email will be sent
 password i.e., the app password which has generated in previous step
 to i.e., recipient's email id

13. Develop the playbook with the module "community.general.mail" and run it. If the configuration is done correctly, then you will find the test email in the recipient's mail box.
