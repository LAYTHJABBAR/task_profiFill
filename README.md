# Job Management Dashboard

## Project Overview

The goal of this project was to create a job management dashboard with a Node.js backend and a React frontend. The project requirements included creating a REST API for managing job data and a frontend to interact with the API.

## Key Decisions and Approach

### Backend Development

1. **Technology Stack**:
   - **Node.js**: Chosen for its scalability and ease of use in building RESTful APIs.
   - **Express**: A lightweight framework for setting up the server and routing.
   - **TypeScript**: Used for type safety and better code quality.
   - **JSON File Storage**: Used to simulate a database for simplicity.

2. **Folder Structure**:
   - `src/models.ts`: Contains the data model and functions to read/write jobs from/to a JSON file.
   - `src/controllers.ts`: Contains the logic for handling API requests (CRUD operations).
   - `src/routes.ts`: Defines the API endpoints and links them to the corresponding controllers.
   - `src/index.ts`: Sets up the Express server and middleware.

3. **Data Handling**:
   - **Date Format**: Ensured all dates are stored and returned in the `2024-06-15T09:00:00Z` format for consistency.
   - **JSON Storage**: Used a JSON file (`data/jobs.json`) to store job data, making it easy to read and write job records.

4. **Security and Error Handling**:
   - Implemented basic error handling for operations like getting a job by ID, updating, and deleting jobs.
   - Used `cors` to handle cross-origin requests, allowing the frontend to communicate with the backend.

### Frontend Development

1. **Technology Stack**:
   - **React**: Chosen for its component-based architecture and ease of building interactive UIs.
   - **TypeScript**: Used for type safety and better code quality.
   - **React Router**: Used for navigation between different views (job list, job details, add/edit job).

2. **Component Structure**:
   - **JobList**: Displays a list of all jobs with options to edit and delete each job.
   - **JobDetail**: Displays detailed information about a selected job with an option to edit the job.
   - **JobForm**: Used for both adding new jobs and editing existing jobs.
   - **Header**: Displays the application title and navigation links.

## Installation

For installation instructions, please visit the [Job Management Backend](./job-management-backend/README.md) and [Job Management Frontend](./job-management-frontend/README.md) folders for more information.

---

## Backend

The backend is responsible for managing the job data and providing a REST API for CRUD operations.

### Setup Instructions

1. **Clone the repository**:
    ```bash
    git clone <repository-url>
    cd job-management-backend
    ```

2. **Install dependencies**:
    ```bash
    npm install
    ```

3. **Run the backend server**:
    ```bash
    npm run dev
    ```

### API Endpoints

- **GET /jobs**: Retrieves all jobs.
- **GET /jobs/:id**: Retrieves a specific job by ID.
- **POST /jobs**: Adds a new job record.
- **PUT /jobs/:id**: Updates an existing job record.
- **DELETE /jobs/:id**: Deletes a job record.

---

## Frontend

The frontend provides a user-friendly interface for interacting with the job data through the REST API.

### Setup Instructions

1. **Clone the repository**:
    ```bash
    git clone <repository-url>
    cd job-management-frontend
    ```

2. **Install dependencies**:
    ```bash
    npm install
    ```

3. **Run the frontend development server**:
    ```bash
    npm start
    ```

### Application Features

- **Job List View**: Displays all jobs in a list format.
- **Job Details View**: Displays detailed information about a specific job.
- **Add Job Form**: Allows users to add new job records.
- **Edit Job Form**: Allows users to edit existing job records.
- **Delete Job**: Allows users to delete job records.

## Components

- **Header**: Displays the application title and navigation links.
- **JobList**: Lists all job records with options to edit and delete.
- **JobDetail**: Displays detailed information about a selected job.
- **JobForm**: Used for both adding new jobs and editing existing jobs.

## Styling

CSS is used for styling components, ensuring a consistent and responsive design. Flexbox is used for layout and alignment of buttons and form elements.

## Handling Dates

Dates are handled using the `datetime-local` input type in forms. Dates are formatted to match the backend's requirements before being sent in API requests.
