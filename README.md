# GetRides 🚗

<div align="center">
  <h3>Your Modern Ride-Sharing Platform</h3>
  <p><strong>Book • Share • Travel</strong></p>
</div>

<img width="1470" height="871" alt="Screenshot 2025-11-07 at 10 32 48 PM" src="https://github.com/user-attachments/assets/928c7ead-b573-4dbe-b0c7-2d6044dd0b4a" />


---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Demo](#-demo)
- [Tech Stack](#️-tech-stack)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
- [Environment Setup](#-environment-setup)
- [Project Structure](#-project-structure)
- [Available Scripts](#-available-scripts)
- [Key Features](#-key-features-in-detail)
- [API Integration](#-api-integration)
- [State Management](#-state-management)
- [Contributing](#-contributing)
- [Roadmap](#-roadmap)
- [License](#-license)

---

## 🌟 Overview

GetRides is a modern, full-featured ride-sharing application built with React and Vite. It provides a seamless experience for both riders and drivers, featuring real-time ride tracking, secure payments, and an intuitive user interface.

**Backend Repository**: [GetRides-backend](https://github.com/Prateet-Github/GetRides-backend) *(if applicable)*

---

## ✨ Features

### For Riders 🙋‍♂️
- 📍 **Live Location Tracking** - Real-time ride tracking with maps integration
- 💳 **Multiple Payment Options** - Card, wallet, and cash payments
- ⭐ **Rating System** - Rate drivers and view ratings
- 🚕 **Ride History** - View all past and upcoming rides
- 💰 **Fare Estimation** - Get instant fare estimates before booking
- 🔔 **Push Notifications** - Real-time ride updates

### For Drivers 🚗
- 📱 **Driver Dashboard** - Manage rides and earnings
- 🗺️ **Route Optimization** - Best routes for pickups and drop-offs
- 💵 **Earnings Tracker** - Track daily, weekly, and monthly earnings
- 👥 **Rider Information** - View rider profiles and ratings
- ⚡ **Quick Accept** - Accept ride requests instantly

### General Features
- 🔐 **Secure Authentication** - JWT-based secure login
- 📱 **Responsive Design** - Works seamlessly on all devices
- 🎨 **Modern UI/UX** - Clean and intuitive interface
- 🌙 **Dark Mode** - Eye-friendly dark theme
- 🌍 **Multi-language Support** - Available in multiple languages
- ♿ **Accessibility** - WCAG compliant

---

## 🎯 Demo

<!-- Add your demo link here -->
**Live Demo**: [Coming Soon]

<!-- Add screenshots here -->
### Screenshots

<!-- 
### Home Screen
![Home Screen](./assets/screenshots/home.png)

### Booking Interface
![Booking](./assets/screenshots/booking.png)

### Ride Tracking
![Tracking](./assets/screenshots/tracking.png)
-->

---

## 🛠️ Tech Stack

| Category | Technology |
|----------|-----------|
| **Framework** | React 18 |
| **Build Tool** | Vite |
| **Routing** | React Router DOM |
| **State Management** | Context API / Redux |
| **Maps Integration** | Google Maps API / Mapbox |
| **HTTP Client** | Axios |
| **Styling** | CSS3 / Tailwind CSS / Styled Components |
| **Real-time** | Socket.IO Client |
| **Form Handling** | React Hook Form |
| **Validation** | Yup / Zod |
| **Icons** | React Icons / Heroicons |
| **Notifications** | React Toastify |
| **Code Quality** | ESLint + Prettier |

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v16.0 or higher)
- **npm** or **yarn** package manager
- **Git**
- **Google Maps API Key** (for maps functionality)

---

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Prateet-Github/GetRides-frontend.git
cd GetRides-frontend
```

### 2. Install Dependencies

```bash
npm install
# or
yarn install
```

### 3. Set Up Environment Variables

Create a `.env` file in the root directory:

```env
# API Configuration
VITE_API_BASE_URL=http://localhost:5000/api
VITE_SOCKET_URL=http://localhost:5000

# Google Maps
VITE_GOOGLE_MAPS_API_KEY=your_google_maps_api_key

# App Configuration
VITE_APP_NAME=GetRides
VITE_APP_VERSION=1.0.0

# Payment Gateway (if applicable)
VITE_STRIPE_PUBLIC_KEY=your_stripe_public_key
VITE_RAZORPAY_KEY=your_razorpay_key

# Firebase (for push notifications, optional)
VITE_FIREBASE_API_KEY=your_firebase_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_auth_domain
VITE_FIREBASE_PROJECT_ID=your_project_id
```

### 4. Start Development Server

```bash
npm run dev
# or
yarn dev
```

The application will open at `http://localhost:5173`

---

## 📁 Project Structure

```
GetRides-frontend/
├── context/              # React Context providers
│   ├── AuthContext.jsx  # Authentication context
│   ├── RideContext.jsx  # Ride management context
│   └── MapContext.jsx   # Maps and location context
├── helper/              # Helper functions
│   ├── api.js          # API utility functions
│   ├── validation.js   # Form validation helpers
│   └── formatters.js   # Data formatting utilities
├── public/             # Static assets
│   ├── icons/         # App icons
│   └── images/        # Images and graphics
├── src/
│   ├── assets/        # Images, fonts, etc.
│   ├── components/    # Reusable components
│   │   ├── common/   # Shared components
│   │   ├── rider/    # Rider-specific components
│   │   └── driver/   # Driver-specific components
│   ├── pages/         # Page components
│   │   ├── Home.jsx
│   │   ├── Login.jsx
│   │   ├── Booking.jsx
│   │   ├── RideTracking.jsx
│   │   └── Profile.jsx
│   ├── hooks/         # Custom React hooks
│   │   ├── useAuth.js
│   │   ├── useLocation.js
│   │   └── useSocket.js
│   ├── services/      # API services
│   │   ├── authService.js
│   │   ├── rideService.js
│   │   └── paymentService.js
│   ├── styles/        # Global styles
│   ├── App.jsx        # Main App component
│   └── main.jsx       # Entry point
├── utils/             # Utility functions
│   ├── constants.js   # App constants
│   ├── helpers.js     # Generic helpers
│   └── socket.js      # Socket.IO setup
├── .env               # Environment variables
├── .eslintrc.js       # ESLint configuration
├── .gitignore         # Git ignore file
├── index.html         # HTML template
├── package.json       # Dependencies
├── vite.config.js     # Vite configuration
└── README.md          # Documentation
```

---

## 📦 Available Scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Start development server |
| `npm run build` | Build for production |
| `npm run preview` | Preview production build |
| `npm run lint` | Run ESLint |
| `npm run lint:fix` | Fix ESLint errors |
| `npm run format` | Format code with Prettier |

---

## 🎯 Key Features in Detail

### 1. Authentication System
- Email/Phone number login
- OTP verification
- Social media login (Google, Facebook)
- JWT token management
- Secure password reset

### 2. Ride Booking Flow
```
Select Pickup → Choose Destination → View Fare → Select Vehicle → Confirm → Track Ride
```

### 3. Real-time Tracking
- Live driver location updates
- Estimated time of arrival (ETA)
- Turn-by-turn navigation
- Route visualization on map

### 4. Payment Integration
- Credit/Debit cards
- Digital wallets
- Cash payment option
- Ride fare breakdown
- Payment history

### 5. User Profiles
- Personal information management
- Ride history
- Saved addresses
- Payment methods
- Emergency contacts

---

## 🔌 API Integration

### Authentication Endpoints
```javascript
// Login
POST /api/auth/login
Body: { email, password }

// Register
POST /api/auth/register
Body: { name, email, phone, password }

// Verify OTP
POST /api/auth/verify-otp
Body: { phone, otp }
```

### Ride Endpoints
```javascript
// Book a ride
POST /api/rides/book
Body: { pickup, destination, vehicleType }

// Get ride details
GET /api/rides/:rideId

// Cancel ride
PUT /api/rides/:rideId/cancel
```

### Example API Call
```javascript
import axios from 'axios';

const bookRide = async (rideData) => {
  try {
    const response = await axios.post(
      `${import.meta.env.VITE_API_BASE_URL}/rides/book`,
      rideData,
      {
        headers: {
          'Authorization': `Bearer ${token}`
        }
      }
    );
    return response.data;
  } catch (error) {
    console.error('Booking failed:', error);
    throw error;
  }
};
```

---

## 🔄 State Management

### Context Structure
```javascript
// AuthContext - Manages user authentication
const AuthContext = createContext();

// RideContext - Manages ride state
const RideContext = createContext();

// MapContext - Manages map and location
const MapContext = createContext();
```

### Using Context
```javascript
import { useAuth } from '../context/AuthContext';

function MyComponent() {
  const { user, login, logout } = useAuth();
  
  return (
    <div>
      {user ? `Welcome ${user.name}` : 'Please login'}
    </div>
  );
}
```

---

## 🗺️ Maps Integration

### Google Maps Setup
```javascript
import { GoogleMap, Marker, DirectionsRenderer } from '@react-google-maps/api';

const MapComponent = ({ origin, destination }) => {
  const [directions, setDirections] = useState(null);

  useEffect(() => {
    // Calculate route
    const directionsService = new google.maps.DirectionsService();
    
    directionsService.route(
      {
        origin,
        destination,
        travelMode: google.maps.TravelMode.DRIVING
      },
      (result, status) => {
        if (status === 'OK') {
          setDirections(result);
        }
      }
    );
  }, [origin, destination]);

  return (
    <GoogleMap
      zoom={12}
      center={origin}
    >
      {directions && <DirectionsRenderer directions={directions} />}
    </GoogleMap>
  );
};
```

---

## 🧪 Testing

```bash
# Run tests
npm run test

# Run tests with coverage
npm run test:coverage

# Run tests in watch mode
npm run test:watch
```

---

## 🚀 Deployment

### Deploy to Vercel

1. **Install Vercel CLI**
   ```bash
   npm i -g vercel
   ```

2. **Deploy**
   ```bash
   vercel
   ```

### Deploy to Netlify

1. **Build the project**
   ```bash
   npm run build
   ```

2. **Deploy via Netlify CLI**
   ```bash
   npm i -g netlify-cli
   netlify deploy --prod
   ```

### Environment Variables
Remember to set all environment variables in your deployment platform's dashboard.

---

## 🤝 Contributing

Contributions are welcome! Follow these steps:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Commit your changes**
   ```bash
   git commit -m 'Add amazing feature'
   ```
4. **Push to the branch**
   ```bash
   git push origin feature/amazing-feature
   ```
5. **Open a Pull Request**

### Code Style Guidelines
- Use functional components with hooks
- Follow ESLint configuration
- Write meaningful commit messages
- Add comments for complex logic
- Update documentation as needed

---

## 🗺️ Roadmap

- [ ] Real-time ride sharing
- [ ] In-app chat between rider and driver
- [ ] Scheduled rides
- [ ] Carpooling feature
- [ ] Ride split payment
- [ ] Driver earnings analytics
- [ ] Multi-city support
- [ ] Progressive Web App (PWA)
- [ ] Offline mode
- [ ] AI-based fare optimization

---

## 🐛 Bug Reports & Feature Requests

Found a bug or have a feature request? Please open an issue on [GitHub Issues](https://github.com/Prateet-Github/GetRides-frontend/issues).

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Prateet**
- GitHub: [@Prateet-Github](https://github.com/Prateet-Github)
- Frontend: [GetRides-frontend](https://github.com/Prateet-Github/GetRides-frontend)

---

## 🙏 Acknowledgments

- React team for the amazing framework
- Vite team for the lightning-fast build tool
- Google Maps API for mapping capabilities
- All open-source contributors

---

## 📞 Support

For support and queries:
- Open an issue on GitHub
- Contact through GitHub profile

---

<div align="center">
  <p>⭐ If you like this project, please give it a star on GitHub! ⭐</p>
  <p>Made with ❤️ by Prateet</p>
</div>
