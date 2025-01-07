# Strapi Backend for AI Resume Builder

This repository contains the Strapi backend used for the AI Resume Builder application. The backend manages user data, connects to Neon Postgres for storage, and provides APIs for the frontend to interact with.

## Features
- **API Management:** Provides secure endpoints for the frontend to handle user data.
- **Database Integration:** Uses Neon Postgres for storing and retrieving user information.
- **Authentication:** Integrated with Clerk for user authentication and authorization.
- **AI Integration:** Facilitates communication with Gemini AI for natural language processing tasks.
- **Payment Gateway Support:** APIs to handle Razorpay and PayPal integration.

## Technologies Used
- **Backend Framework:** Strapi
- **Database:** Neon Postgres
- **Authentication:** Clerk
- **AI:** Gemini API
- **Payment Gateways:** Razorpay, PayPal

## Installation

### Prerequisites
- Node.js (v18 or higher)
- npm or yarn
- Neon Postgres account

### Steps to Set Up the Backend

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/adarshpheonix2810/Ai-resume-builder-strapi-admin.git
   cd Ai-resume-builder-strapi-admin
   ```

2. **Install Dependencies:**
   ```bash
   npm install
   ```

3. **Set Up Environment Variables:**
   Create a `.env` file in the root directory and add the following:
   ```env
   DATABASE_URL=<your-neon-postgres-url>
   CLERK_API_KEY=<your-clerk-api-key>
   GEMINI_API_KEY=<your-gemini-api-key>
   PAYPAL_CLIENT_ID=<your-paypal-client-id>
   RAZORPAY_KEY=<your-razorpay-key>
   ```
   Replace the placeholders with your actual credentials.

4. **Start Strapi in Development Mode:**
   ```bash
   npm run develop
   # or
   yarn develop
   ```
   Strapi will run on `http://localhost:1337` by default.

5. **Build for Production:**
   To build and start Strapi in production mode:
   ```bash
   npm run build
   npm run start
   # or
   yarn build
   yarn start
   ```

### Deployment

Strapi provides multiple deployment options, including [Strapi Cloud](https://cloud.strapi.io). Follow these steps for deployment:

1. **Choose a Deployment Platform:**
   - Platforms like Heroku, Vercel, DigitalOcean, or AWS can be used.

2. **Set Environment Variables:**
   Configure the same `.env` variables from your local setup in the deployment platform's environment settings.

3. **Run the Application:**
   Start the Strapi application as per the platform’s deployment guidelines.

   For example, if using Strapi Cloud:
   ```bash
   yarn strapi deploy
   ```

## API Endpoints

### Authentication
- **Register/Login**: Handles user authentication using Clerk.

### Resume Management
- **GET /resumes**: Fetch all resumes for a user.
- **POST /resumes**: Create a new resume.
- **PUT /resumes/:id**: Update an existing resume.
- **DELETE /resumes/:id**: Delete a resume.

### AI Integration
- **POST /ai/generate-summary**: Generate a professional summary using Gemini AI.

### Payment Gateway
- **POST /payment/razorpay**: Initiate a Razorpay payment.
- **POST /payment/paypal**: Initiate a PayPal payment.

## 📚 Learn More

- [Resource center](https://strapi.io/resource-center) - Strapi resource center.
- [Strapi documentation](https://docs.strapi.io) - Official Strapi documentation.
- [Strapi tutorials](https://strapi.io/tutorials) - List of tutorials made by the core team and the community.
- [Strapi blog](https://strapi.io/blog) - Official Strapi blog containing articles made by the Strapi team and the community.
- [Changelog](https://strapi.io/changelog) - Find out about Strapi product updates, new features, and general improvements.

Feel free to check out the [Strapi GitHub repository](https://github.com/strapi/strapi). Your feedback and contributions are welcome!

## ✨ Community

- [Discord](https://discord.strapi.io) - Chat with the Strapi community and core team.
- [Forum](https://forum.strapi.io/) - Discuss, ask questions, find answers, showcase your Strapi project, and get feedback.
- [Awesome Strapi](https://github.com/strapi/awesome-strapi) - A curated list of awesome things related to Strapi.

## Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes. Ensure that your code adheres to the project’s coding standards.

## License
This project is licensed under the [MIT License](LICENSE). See the LICENSE file for more details.

