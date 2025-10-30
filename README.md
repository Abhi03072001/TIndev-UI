# Tindev Frontend

## Setup Instructions

1. Install dependencies:
```bash
npm install
```

2. Start the development server:
```bash
npm run dev
```

The frontend will run on `http://localhost:5173`

## Fixed Issues

1. **Field name mismatch**: Fixed `emailId` to `email` in login/signup requests
2. **Authentication flow**: Added proper error handling for unauthorized requests
3. **Navigation**: Prevented infinite redirects when already on login page

## Testing the Application

1. Open `http://localhost:5173` in your browser
2. You should be redirected to the login page if not authenticated
3. Create a new account or login with existing credentials
4. After successful login, you'll be redirected to the main feed

## Common Issues

- **Unauthorized Error**: This is normal behavior when not logged in. The app will redirect to login.
- **CORS Error**: Make sure the backend server is running on port 3000
- **Network Error**: Check if both frontend and backend are running

## Development

- The app uses Redux for state management
- React Router for navigation
- Axios for API calls with credentials enabled
- Tailwind CSS for styling










# Deployment

- Signup on AWS 
- Launch instance
- chmod 400 <secret>.pem(for windows its different)
- ssh -i (take the command from ec2 instance)
- Install Node version (in which version your project built)
- Git clone
- Frontend    
    - npm install  -> dependencies install
    - npm run build
    - sudo apt update
    #for install start and enable nginx
    - sudo apt install nginx
    - sudo systemctl start nginx
    - sudo systemctl enable nginx
    - Copy code from dist(build files) to /var/www/html/
    - sudo scp -r dist/* /var/www/html/
    - Enable port :80 of your instance
