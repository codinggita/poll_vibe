Backend Deployed Link : https://poll-vibe-backend.onrender.com
Postman DOcs : https://documenter.getpostman.com/view/39216490/2sAYk8uhq8

![image](https://github.com/user-attachments/assets/645ca56e-c848-4a06-a133-f04e11c00954)
![image](https://github.com/user-attachments/assets/48305587-8d1a-4540-b192-a6f2f158001e)

# Poll Vibe 📊

A modern, real-time polling application that enables users to create interactive polls, vote on decisions, and view live results. Built with a full-stack architecture using React and Node.js.

## 🎯 Overview

Poll Vibe is a comprehensive polling platform designed for making collaborative decisions through community voting. Whether you're choosing outfits, gathering opinions, conducting surveys, or making group decisions, Poll Vibe makes it easy to create polls and collect instant feedback from your audience.

## ✨ Features

### Core Functionality
- **Create Polls Instantly**: Set up polls with multiple options in seconds
- **Real-Time Voting**: See votes come in live as participants respond
- **Beautiful Visualizations**: View poll results with intuitive charts and graphs
- **Vote on Community Polls**: Browse and participate in polls created by others
- **User Authentication**: Secure login and registration system
- **Poll Management**: Edit, delete, and manage your created polls
- **Anonymous Voting**: Option for users to vote anonymously
- **Share Polls**: Easy sharing via links for maximum reach

### User Experience
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Intuitive Interface**: Clean, modern UI for easy navigation
- **Instant Feedback**: Get immediate results as votes are cast
- **Poll Discovery**: Explore trending and popular polls from the community

## 🏗️ Architecture

```
┌─────────────┐
│   Frontend  │ (React, CSS, HTML)
│  (Client)   │
└──────┬──────┘
       │
       │ HTTP/REST API
       │
       ▼
┌─────────────┐
│   Backend   │ (Node.js, Express)
│   (API)     │
└──────┬──────┘
       │
       ▼
┌─────────────┐
│  Database   │ (MongoDB/PostgreSQL)
└─────────────┘
```

## 🛠️ Technology Stack

### Frontend
- **Framework**: React.js
- **Styling**: CSS3 with modern design patterns
- **State Management**: React Hooks
- **HTTP Client**: Axios/Fetch API
- **Routing**: React Router

### Backend
- **Runtime**: Node.js
- **Framework**: Express.js
- **Language**: JavaScript/TypeScript
- **Authentication**: JWT (JSON Web Tokens)
- **API Documentation**: Postman

### Database
- **Database**: MongoDB/PostgreSQL
- **ODM/ORM**: Mongoose/Sequelize

## 📋 Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- MongoDB or PostgreSQL database
- Git

## 🚀 Getting Started

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/codinggita/poll_vibe.git
   cd poll_vibe
   ```

2. **Install Backend Dependencies**
   ```bash
   cd Backend
   npm install
   ```

3. **Install Frontend Dependencies**
   ```bash
   cd ../Frontend
   npm install
   ```

### Configuration

4. **Setup Backend Environment Variables**
   
   Create a `.env` file in the `Backend` directory:
   
   ```env
   # Server Configuration
   PORT=5000
   NODE_ENV=development
   
   # Database
   DB_CONNECTION_STRING=mongodb://localhost:27017/poll_vibe
   # OR for PostgreSQL
   # DB_CONNECTION_STRING=postgresql://username:password@localhost:5432/poll_vibe
   
   # Authentication
   JWT_SECRET=your_jwt_secret_key_here
   JWT_EXPIRY=24h
   
   # CORS
   CORS_ORIGIN=http://localhost:3000
   ```

5. **Setup Frontend Environment Variables**
   
   Create a `.env` file in the `Frontend` directory:
   
   ```env
   REACT_APP_API_URL=http://localhost:5000/api
   REACT_APP_API_BASE_URL=http://localhost:5000
   ```

### Running the Application

6. **Start the Backend Server**
   ```bash
   cd Backend
   npm start
   # or for development with hot reload
   npm run dev
   ```

7. **Start the Frontend Application**
   ```bash
   cd Frontend
   npm start
   ```

8. **Access the Application**
   - Frontend: `http://localhost:3000`
   - Backend API: `http://localhost:5000`
   - API Documentation: [Postman Docs](https://documenter.getpostman.com/view/39216490/2sAYk8uhq8)

## 🌐 Deployment

### Live Deployment
- **Backend API**: [https://poll-vibe-backend.onrender.com](https://poll-vibe-backend.onrender.com)
- **API Documentation**: [Postman Docs](https://documenter.getpostman.com/view/39216490/2sAYk8uhq8)

### Deploying to Production

**Backend (Render/Heroku/Railway)**
1. Push your code to GitHub
2. Connect your repository to your hosting platform
3. Set environment variables in the platform dashboard
4. Deploy the application

**Frontend (Vercel/Netlify)**
1. Build the production bundle:
   ```bash
   cd Frontend
   npm run build
   ```
2. Deploy the `build` folder to your hosting platform
3. Configure environment variables for production API URL

## 📚 API Documentation

Comprehensive API documentation is available on Postman:
- **[View API Docs](https://documenter.getpostman.com/view/39216490/2sAYk8uhq8)**

### Key API Endpoints

```
Authentication:
POST   /api/auth/register        - Register new user
POST   /api/auth/login           - User login
GET    /api/auth/profile         - Get user profile

Polls:
GET    /api/polls                - Get all polls
POST   /api/polls                - Create new poll
GET    /api/polls/:id            - Get specific poll
PUT    /api/polls/:id            - Update poll
DELETE /api/polls/:id            - Delete poll

Voting:
POST   /api/polls/:id/vote       - Cast a vote
GET    /api/polls/:id/results    - Get poll results
```

## 🎮 Usage

### Creating a Poll
1. Sign up or log in to your account
2. Click "Create Poll" button
3. Enter your poll question
4. Add poll options (minimum 2 options)
5. Configure poll settings (anonymous voting, expiry, etc.)
6. Click "Create" to publish your poll
7. Share the poll link with your audience

### Voting on Polls
1. Browse available polls on the homepage
2. Click on a poll to view details
3. Select your preferred option
4. Submit your vote
5. View real-time results

### Managing Your Polls
1. Navigate to "My Polls" section
2. View all polls you've created
3. Edit or delete polls as needed
4. Track voting statistics and engagement

## 📊 MVP Checklist

Based on the project development:

✅ User authentication (Register/Login)  
✅ Create polls with multiple options  
✅ Vote on polls  
✅ View real-time poll results  
✅ Browse community polls  
✅ Responsive design  
✅ Backend API with Express.js  
✅ Frontend with React  
✅ Database integration  
✅ RESTful API architecture  
✅ Deployed backend on Render  
✅ API documentation on Postman  

## 🔮 Future Enhancements

- [ ] Real-time updates with WebSockets/Socket.IO
- [ ] Poll categories and tags
- [ ] Advanced analytics dashboard
- [ ] Comment system for polls
- [ ] Poll sharing on social media
- [ ] Image/media support in poll options
- [ ] Poll templates
- [ ] Email notifications
- [ ] Multi-language support
- [ ] Dark mode theme
- [ ] Export poll results (PDF, CSV)
- [ ] Scheduled poll expiration
- [ ] Private/public poll options
- [ ] Poll embedding for external websites

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Contribution Guidelines
- Follow the existing code style
- Write meaningful commit messages
- Update documentation as needed
- Add tests for new features
- Ensure all tests pass before submitting PR

## 📸 Screenshots

![Poll Vibe Landing](https://private-user-images.githubusercontent.com/177345657/418263214-645ca56e-c848-4a06-a133-f04e11c00954.png)
*Landing page with featured polls*

![Create Poll](https://private-user-images.githubusercontent.com/177345657/418263237-48305587-8d1a-4540-b192-a6f2f158001e.png)
*Create poll interface*

![MVP Checklist](https://private-user-images.githubusercontent.com/177345657/420354028-4717b7a1-d71a-475b-a0e8-2289894b7237.png)
*MVP development progress*

## 🐛 Known Issues

Check the [Issues](https://github.com/codinggita/poll_vibe/issues) page for known bugs and feature requests.

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Team

- **Organization**: [codinggita](https://github.com/codinggita)
- **Contributors**: See [Contributors](https://github.com/codinggita/poll_vibe/graphs/contributors)

## 🌟 Support

If you find this project helpful, please give it a ⭐️ on GitHub!

## 📧 Contact

- **Repository**: [https://github.com/codinggita/poll_vibe](https://github.com/codinggita/poll_vibe)
- **Issues**: [Report a bug](https://github.com/codinggita/poll_vibe/issues)
- **Pull Requests**: [Submit a PR](https://github.com/codinggita/poll_vibe/pulls)

## 🙏 Acknowledgments

- Inspired by modern polling platforms like Poll Everywhere, Slido, and Mentimeter
- Built with React and Node.js ecosystem
- Deployed on Render for reliable hosting
- Community-driven feature development

---

Made with ❤️ by the codinggita team

**Happy Polling! 📊✨**

MVP CheckList
![image](https://github.com/user-attachments/assets/4717b7a1-d71a-475b-a0e8-2289894b7237)
