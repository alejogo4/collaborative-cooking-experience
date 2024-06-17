### Detailed Technical Test Instructions for Fullstack Developer

#### Objective

Create a multi-platform application that allows users to participate in a real-time collaborative cooking experience. The application should have a web interface (Next.js) and a mobile interface (React Native). The backend will be powered by Node.js with Nest.js and should be containerized using Docker.

### Project Overview

#### Features

1.  **User Authentication**:
    
    *   Implement user registration and login functionality.
    *   Ensure that only authenticated users can create or join recipes.
2.  **Recipe Creation and Collaboration**:
    
    *   Users can create new recipes or join existing ones using a unique code.
    *   Users can contribute by adding ingredients, steps, and tips in real-time.
3.  **Real-time Collaboration**:
    
    *   Ensure that updates to the recipe are reflected in real-time across all connected clients using WebSockets.
4.  **Recipe Timeline**:
    
    *   Display the recipe timeline with contributions from different users.
    *   Highlight the current step being edited.
5.  **Notifications**:
    
    *   Notify users when a new ingredient, step, or tip is added or when they receive a mention in a recipe.

### Technical Requirements

#### Frontend (Next.js)

*   **Pages**:
    
    *   `/login`: User login page.
    *   `/register`: User registration page.
    *   `/recipes`: Main page to view and manage recipes.
    *   `/recipes/:id`: Page to view and contribute to a specific recipe.
*   **Components**:
    
    *   `RecipeList`: Displays a list of recipes.
    *   `RecipeItem`: Represents an individual recipe.
    *   `RecipeEditor`: Interface for adding ingredients, steps, and tips to a recipe.
    *   `Notification`: Shows real-time notifications.
*   **Styling**:
    
    *   Use Tailwind CSS for styling.

**Detailed Tasks**:

1.  **Login Page**:
    
    *   Create a form to input username and password.
    *   On successful login, redirect to the `/recipes` page.
2.  **Register Page**:
    
    *   Create a form to input username, email, and password.
    *   On successful registration, redirect to the `/login` page.
3.  **Recipes Page**:
    
    *   Display a list of recipes using the `RecipeList` component.
    *   Provide a button to create a new recipe.
4.  **Recipe Details Page**:
    
    *   Display the recipe details including ingredients, steps, and tips.
    *   Use `RecipeEditor` to allow users to add ingredients, steps, and tips.
    *   Show real-time updates using WebSockets.

#### Mobile (React Native)

*   **Screens**:
    
    *   `LoginScreen`: User login screen.
    *   `RegisterScreen`: User registration screen.
    *   `RecipeListScreen`: Main screen to view and manage recipes.
    *   `RecipeScreen`: Screen to view and contribute to a specific recipe.
*   **Components**:
    
    *   `RecipeList`: Displays a list of recipes.
    *   `RecipeItem`: Represents an individual recipe.
    *   `RecipeEditor`: Interface for adding ingredients, steps, and tips to a recipe.
    *   `Notification`: Shows real-time notifications.
*   **Navigation**:
    
    *   Use React Navigation for handling screen transitions.

**Detailed Tasks**:

1.  **Login Screen**:
    
    *   Create a form to input username and password.
    *   On successful login, navigate to the `RecipeListScreen`.
2.  **Register Screen**:
    
    *   Create a form to input username, email, and password.
    *   On successful registration, navigate to the `LoginScreen`.
3.  **Recipe List Screen**:
    
    *   Display a list of recipes using the `RecipeList` component.
    *   Provide a button to create a new recipe.
4.  **Recipe Details Screen**:
    
    *   Display the recipe details including ingredients, steps, and tips.
    *   Use `RecipeEditor` to allow users to add ingredients, steps, and tips.
    *   Show real-time updates using WebSockets.

#### Backend (Nest.js)

*   **Modules**:
    
    *   `AuthModule`: Handles user authentication.
    *   `RecipeModule`: Manages CRUD operations for recipes.
    *   `IngredientModule`: Manages CRUD operations for ingredients.
    *   `StepModule`: Manages CRUD operations for steps.
    *   `TipModule`: Manages CRUD operations for tips.
    *   `NotificationModule`: Manages real-time notifications using WebSockets.
*   **Database**:
    
    *   Use a relational database (e.g., PostgreSQL) to store user, recipe, ingredient, step, and tip data.
*   **Authentication**:
    
    *   Use JWT for securing endpoints.

**Detailed Tasks**:

1.  **Auth Module**:
    
    *   Implement endpoints for user registration and login.
    *   Use JWT for authentication and securing routes.
2.  **Recipe Module**:
    
    *   Implement CRUD operations for recipes.
    *   Allow users to create and join recipes using a unique code.
3.  **Ingredient Module**:
    
    *   Implement CRUD operations for ingredients.
4.  **Step Module**:
    
    *   Implement CRUD operations for steps.
5.  **Tip Module**:
    
    *   Implement CRUD operations for tips.
6.  **Notification Module**:
    
    *   Implement real-time notifications using WebSockets.

#### Docker

*   **Dockerfile**:
    
    *   Create Dockerfiles for the frontend, mobile, and backend services.
*   **Docker Compose**:
    
    *   Create a `docker-compose.yml` file to orchestrate the multi-container setup.

**Detailed Tasks**:

1.  **Dockerfile for Frontend**:
    
    *   Create a Dockerfile for the Next.js application.
2.  **Dockerfile for Mobile**:
    
    *   Create a Dockerfile for the React Native application.
3.  **Dockerfile for Backend**:
    
    *   Create a Dockerfile for the Nest.js application.
4.  **Docker Compose Setup**:
    
    *   Create a `docker-compose.yml` file to run all services together.
    *   Ensure services can communicate with each other within the Docker network.

### Deliverables

*   A GitHub repository with the complete source code.
*   Detailed setup instructions in the `README.md` file.
*   Docker images for each service uploaded to a container registry (e.g., Docker Hub).

### Evaluation Criteria

*   **Code Quality**: Clean, readable, and well-documented code.
*   **Functionality**: The application meets the specified requirements and features.
*   **Creativity**: Interesting and innovative implementation details.
*   **Dockerization**: Correctly configured and functional Docker setup.
*   **Real-time Collaboration**: Efficient implementation of real-time updates and notifications.

This technical test aims to challenge your fullstack development skills and your ability to integrate various technologies into a cohesive, creative, and engaging application. Good luck!