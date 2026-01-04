# Saarthi Travel Itinerary

A Flask-based web application that helps users discover travel routes and itineraries for various cities. Saarthi (meaning "guide" or "companion" in Hindi) serves as your travel companion, providing route information and collecting user feedback.

## Features

- 🗺️ **Route Discovery**: Search for travel routes and itineraries by city name
- 👤 **User Authentication**: Sign up and login functionality for personalized experience
- 💬 **Feedback System**: Submit and manage travel feedback
- 📊 **Admin Dashboard**: View and manage user feedback with delete options
- 🎨 **Responsive Design**: Clean and user-friendly interface

## Tech Stack

- **Backend**: Flask 3.0.3
- **Frontend**: HTML, CSS (with Jinja2 templating)
- **Data Storage**: CSV files for routes and feedback
- **Authentication**: Flask session management
- **Deployment**: Configured for Vercel deployment

## Project Structure

```
Saarthi_Travel_Itinerary/
├── app.py                  # Main Flask application
├── index.py                # Entry point for Vercel deployment
├── wsgi.py                 # WSGI configuration
├── requirements.txt        # Python dependencies
├── vercel.json            # Vercel deployment configuration
├── data/
│   ├── routes.csv         # Travel routes database
│   └── feedback.csv       # User feedback storage
├── static/
│   └── styles.css         # Application styling
└── templates/
    ├── index.html         # Home page
    ├── results.html       # Search results page
    ├── login.html         # Login page
    ├── signup.html        # Registration page
    ├── feedback.html      # Feedback form
    ├── thank_you.html     # Feedback confirmation
    └── view_feedback.html # Admin feedback view
```

## Installation

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/Saarthi_Travel_Itinerary.git
   cd Saarthi_Travel_Itinerary
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Update secret key**
   - Open `app.py`
   - Replace `'your_secret_key'` with a secure secret key

5. **Run the application**
   ```bash
   python app.py
   ```

6. **Access the application**
   - Open your browser and navigate to `http://localhost:5000`

## Usage

### For Users

1. **Search Routes**: Enter a city name on the home page to discover available travel routes
2. **Sign Up/Login**: Create an account or log in to access personalized features
3. **Submit Feedback**: Share your travel experiences and suggestions

### For Admins

1. Navigate to `/view_feedback` to view all user feedback
2. Delete inappropriate or outdated feedback entries

## Data Files

### routes.csv
Contains travel route information with the following structure:
```
City, Route Details...
```

### feedback.csv
Stores user feedback with the following structure:
```
Name, Email, Feedback
```

## Deployment

This project is configured for deployment on Vercel.

### Deploy to Vercel

1. Install Vercel CLI
   ```bash
   npm i -g vercel
   ```

2. Deploy
   ```bash
   vercel
   ```

The `vercel.json` configuration file is already set up for Python deployment.

## Configuration

### Environment Variables

For production deployment, set the following environment variables:

- `SECRET_KEY`: Your Flask secret key
- `FLASK_ENV`: Set to `production` for production deployment

## Security Notes

⚠️ **Important**: This application uses in-memory storage for user credentials (demonstration purposes only). For production use:

1. Implement a proper database (PostgreSQL, MySQL, SQLite)
2. Hash passwords using libraries like `bcrypt` or `werkzeug.security`
3. Use environment variables for sensitive configuration
4. Implement CSRF protection
5. Add input validation and sanitization

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Future Enhancements

- [ ] Database integration for persistent user data
- [ ] Password hashing and secure authentication
- [ ] Advanced route filtering and search
- [ ] User profiles and saved routes
- [ ] Integration with travel APIs for real-time data
- [ ] Mobile-responsive design improvements
- [ ] Email notifications for feedback
- [ ] Admin authentication and role-based access

## License

This project is open source and available under the [MIT License](LICENSE).

## Contact

For questions or suggestions, please open an issue on GitHub.

---

**Made with ❤️ for travelers**
