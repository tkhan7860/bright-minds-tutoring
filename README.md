# BrightMind Tutoring Website

A production-ready Flask website for BrightMind Tutoring business.

## Features

- **Home Page**: Business introduction and overview
- **Services Page**: Comprehensive list of tutoring subjects
- **Contact Page**: Inquiry form and contact information
- **Google Reviews Section**: Placeholder for reviews integration
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Professional Styling**: Clean, modern design suitable for a tutoring business

## Project Structure

```
bright-minds-tutoring/
├── app.py                 # Flask application
├── requirements.txt       # Python dependencies
├── templates/            # Jinja2 HTML templates
│   ├── base.html         # Base template with navigation
│   ├── index.html        # Home page
│   ├── services.html     # Services page
│   └── contact.html      # Contact page
└── static/
    └── css/
        └── style.css     # Stylesheet
```

## Installation

1. **Create a virtual environment** (recommended):
   ```bash
   python -m venv venv
   ```

2. **Activate the virtual environment**:
   - On Windows:
     ```bash
     venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source venv/bin/activate
     ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

## Running the Application

1. **Make sure your virtual environment is activated**

2. **Run the Flask app**:
   ```bash
   python app.py
   ```

3. **Open your browser** and navigate to:
   ```
   http://localhost:5000
   ```

The application will run in debug mode, so any changes to the code will automatically reload the server.

## Pages

- **Home** (`/`): Welcome page with business introduction and features
- **Services** (`/services`): List of all tutoring subjects offered
- **Contact** (`/contact`): Contact form and business information

## Contact Information

- **Email**: info@brightmindstutoring.com

## Notes

- The contact form currently displays a success message but does not send emails. To add email functionality, you would need to integrate an email service like SendGrid, Mailgun, or SMTP.
- The Google Reviews section includes a placeholder iframe. Replace it with your actual Google Maps/Reviews embed code.
- For production deployment, change the `secret_key` in `app.py` to a secure random value.
- Set `debug=False` in production for security.

## Production Deployment

Before deploying to production:

1. Change `app.secret_key` to a secure random string
2. Set `debug=False` in `app.run()`
3. Use a production WSGI server like Gunicorn or uWSGI
4. Configure environment variables for sensitive data
5. Set up proper email handling for the contact form

