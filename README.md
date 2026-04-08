# AI-Powered-Teeth-Detection-and-Analysis-System

An intelligent web application that leverages computer vision and machine learning to provide automated dental image analysis and detection. Built with Django, React, and OpenCV.

![JUTeeth](./gfg_dummy_pic.png)

## 📋 Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

## ✨ Features

- **Advanced Image Processing**: Automated dental image analysis using OpenCV and computer vision algorithms
- **AI-Powered Detection**: Machine learning models for accurate teeth detection and analysis
- **Cloud Integration**: Google Cloud APIs for secure authentication and scalable infrastructure
- **Interactive Dashboard**: Modern React-based user interface with Redux state management
- **RESTful API**: Comprehensive REST API built with Django REST Framework
- **PDF Report Generation**: Automated generation of patient analysis reports
- **Real-time Processing**: Fast, efficient image processing pipeline
- **Responsive Design**: Mobile-friendly UI built with Chakra UI
- **Docker Support**: Containerized deployment for easy scaling

## 🛠️ Tech Stack

### Backend
- **Framework**: Django 4.1.2
- **API**: Django REST Framework 3.14.0
- **Language**: Python 3.9
- **Image Processing**: OpenCV 4.6.0, Pillow 9.2.0
- **Cloud**: Google Cloud APIs (Vision, Auth, OAuth)

### Frontend
- **Library**: React 17.0.2
- **State Management**: Redux with Redux Thunk
- **UI Framework**: Chakra UI 1.6.8
- **Build Tool**: Webpack 5.44.0
- **Transpiler**: Babel 7.9.0

### Infrastructure
- **Containerization**: Docker
- **Database**: SQLite (default)
- **CORS**: django-cors-headers

### Additional Libraries
- NumPy 1.23.4 - Numerical computations
- fpdf 1.7.2 - PDF generation
- Formik 2.2.9 - Form management
- Framer Motion 4.1.17 - Animations

## 📁 Project Structure
ju_te-main/
│
├── 📄 Root Configuration Files
│   ├── package.json                    # Node.js dependencies and scripts
│   ├── package-lock.json              # Locked npm dependencies
│   ├── requirements.txt                # Python/pip dependencies
│   ├── Pipfile                         # Python pipenv configuration
│   ├── Pipfile.lock                    # Locked pipenv dependencies
│   ├── manage.py                       # Django management script
│   ├── Dockerfile                      # Docker containerization config
│   ├── Procfile                        # Heroku deployment config
│   ├── webpack.config.js               # Webpack bundler config
│   ├── .babelrc                        # Babel transpiler config
│   ├── .gitignore                      # Git ignore rules
│   ├── README.md                       # Project documentation
│   ├── Aptfile                         # System dependencies
│   └── credentials.json                # Google Cloud credentials
│
├── 🔧 teeth/ (Main Django Project)
│   ├── __init__.py
│   ├── settings.py                     # Django settings & configuration
│   ├── urls.py                         # Main URL routing
│   ├── wsgi.py                         # WSGI application entry
│   └── asgi.py                         # ASGI application entry
│
├── 🎨 frontend/ (Django App - Frontend Logic)
│   ├── migrations/
│   │   └── __init__.py                 # Django migrations
│   ├── src/ (React Frontend)
│   │   ├── components/
│   │   │   ├── App.js                  # Main React component
│   │   │   ├── page/
│   │   │   │   └── Main.js             # Main page component
│   │   │   ├── layout/
│   │   │   │   └── Header.js           # Header/Navigation component
│   │   │   ├── engine/
│   │   │   │   ├── Form.js             # Image upload form component
│   │   │   │   ├── Result.js           # Analysis results display
│   │   │   │   ├── ToothWrapper.js     # Tooth analysis visualization
│   │   │   │   ├── Loading.js          # Loading state component
│   │   │   │   └── Error.js            # Error handling component
│   │   ├── actions/
│   │   │   ├── engine.js               # Redux action creators
│   │   │   └── types.js                # Redux action types
│   │   ├── reducers/
│   │   │   └── engine.js               # Redux reducer logic
│   │   ├── store.js                    # Redux store configuration
│   │   ├── theme.js                    # Chakra UI theme customization
│   │   └── index.js                    # React entry point
│   ├── templates/
│   │   └── frontend/
│   │       └── index.html              # Base HTML template
│   ├── static/ (Compiled frontend assets)
│   │   └── frontend/
│   │       └── main.js                 # Compiled React bundle
│   ├── __init__.py
│   ├── apps.py                         # Django app config
│   ├── models.py                       # Database models
│   ├── views.py                        # Django views/API endpoints
│   ├── urls.py                         # Frontend URL routing
│   ├── admin.py                        # Django admin configuration
│   └── tests.py                        # Unit tests
│
├── 🧠 engine/ (ML/AI Processing Engine)
│   ├── migrations/
│   │   ├── __init__.py
│   │   └── 0001_initial.py             # Initial database migration
│   ├── process/ (Computer Vision Processing)
│   │   ├── __init__.py
│   │   ├── buccal.py                   # Buccal view processing
│   │   ├── distal.py                   # Distal view processing
│   │   ├── mesial.py                   # Mesial view processing
│   │   ├── lingual.py                  # Lingual view processing
│   │   ├── top_view.py                 # Top view processing
│   │   └── utils.py                    # Shared processing utilities
│   ├── static/
│   │   └── engine/ (Reference Images)
│   │       ├── buccal-perfect-central.jpg
│   │       ├── buccal-perfect-premandibular.jpg
│   │       ├── distal-perfect-central.jpg
│   │       ├── distal-perfect-premandibular.jpg
│   │       ├── mesial-perfect-premandibular.jpg
│   │       ├── lingual-perfect-premandibular.jpeg
│   │       ├── top_view-perfect-central.jpg
│   │       └── top_view-perfect-premandibular.jpg
│   ├── __init__.py
│   ├── apps.py                         # Django app config
│   ├── models.py                        # Database models for analysis
│   ├── views.py                        # API endpoints for processing
│   ├── admin.py                        # Django admin config
│   └── tests.py                        # Unit tests
│
├── 📁 staticfiles/ (Compiled Static Assets)
│   └── [Compressed frontend assets]
│
├── 📁 media/ (User Uploaded Files)
│   └── [User uploaded images & data]
│
├── 📁 d (Legacy/Utility)
│
└── 📦 Additional Files
    ├── gfg_dummy_pic.png              # Demo image
    ├── w2.png                         # Screenshot/asset
    ├── Window.png                     # Screenshot/asset
    ├── tooth-vision.zip               # Archived data
    └── juteeth-6810962b9c2a.p12       # Google Cloud service key

