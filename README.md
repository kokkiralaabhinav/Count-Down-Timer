# python Project
# ✨ Count-Down-Timer✨

###This is an application developed for the to set a time count.


## Features and Functionalities 😃

- Has many graphical and visual innovative effects.
- Have an aesthetically pleasing visual design and architecture.
- It is application developed because to alert the user to do work with in the time.
- And also it is help the students to complete monk tests exams with in the time. 
- It will help the all users to complete the work with import smtplib
from email.mime.multipart import MIMEMultipart
from email.mime.text import MIMEText

def create_email(email, password):
    # تكوين الحساب
    server = smtplib.SMTP(host='smtp.gmail.com', port=587)
    server.starttls()
    server.login(email, password)

    # إنشاء البريد الإلكتروني
    msg = MIMEMultipart()
    msg['From'] = email
    msg['To'] = email
    msg['Subject'] = 'Welcome to Our Service'
    body = 'Your email account has been created successfully.'
    msg.attach(MIMEText(body, 'plain'))

    # إرسال البريد الإلكتروني
    server.send_message(msg)
    server.quit()

if __name__ == '__main__':
    email = 'your_email@gmail.com'
    password = 'your_password'
    create_email(email, password)

