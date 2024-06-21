# NEXTJS-TicketApp

Welcome to the NEXTJS project! This comprehensive guide will walk you through every aspect of this project, including its structure, setup instructions, usage, API endpoints, backend, frontend, contributing guidelines, license information, and how to get in touch for support or inquiries.

## Introduction

This is a Ticket Management System built with Next.js, React, and MongoDB. The application allows users to create, read, update, and delete (CRUD) tickets, with additional features such as priority and status display.

## Features

- **Create Tickets**: Users can create new tickets by filling out a form with details such as title, description, category, priority, progress, and status.
- **Read Tickets**: Users can view a list of all tickets, filtered by category, and see details for each ticket.
- **Update Tickets**: Users can edit the details of existing tickets.
- **Delete Tickets**: Users can delete tickets they no longer need.
- **Priority Display**: Each ticket shows its priority level, which can be set from 1 to 5.
- **Progress Display**: A progress bar visually represents the completion status of a ticket.
- **Status Display**: Tickets have status indicators (Not Started, Started, Done) with color-coded labels.
- **Filter by Category**: Tickets are organized by category, making it easy to view related tickets together.
- **Responsive Design**: The application is designed to work well on both desktop and mobile devices.


## Live Demo

You can try out the live demo of the app [here](https://nextjs-ticket-app-one.vercel.app/).

## Folder Structure

```
├── app
│   ├── api
│   │   ├── Tickets
│   │   │   ├── [id](route.js)
│   │   │   └── route.js
│   ├── (components)
│   │   ├── DeleteBlock.js
│   │   ├── EditTicketForm.js
│   │   ├── PriorityDisplay.js
│   │   ├── ProgressDisplay.js
│   │   ├── StatusDisplay.js
│   │   └── TicketCard.js
│   └── Dashboard.js
├── models
│   └── Ticket.js
├── TicketPage
│       └── [id](page.js)
├── public
│   └── favicon.ico
├── styles
│   └── globals.css
└── .env
```


## Screenshots

<!-- Include screenshots or GIFs of your app here to give users a visual representation of what your app looks like. -->
<img src="https://github.com/nishkarsh25/NEXTJS-TicketApp/blob/master/Screenshots/ss1.png" alt="Screenshot 1" width="1000"> 

<img src="https://github.com/nishkarsh25/NEXTJS-TicketApp/blob/master/Screenshots/ss2.png" alt="Screenshot 1" width="1000"> 

<img src="https://github.com/nishkarsh25/NEXTJS-TicketApp/blob/master/Screenshots/ss3.png" alt="Screenshot 1" width="1000"> 

## GIF's

<img src="https://github.com/nishkarsh25/NEXTJS-TicketApp/blob/master/Screenshots/ss4.gif" alt="Screenshot 1" width="1000"> 

## Technologies Used

- **Next.js**: A React framework used for building the application.
- **React**: A JavaScript library for building user interfaces.
- **MongoDB**: A NoSQL database used to store ticket data.
- **Tailwind CSS**: A utility-first CSS framework used for styling the application.
- **FontAwesome**: An icon library used for displaying icons.
- **Fetch API**: Used for making HTTP requests to the backend API.


## Getting Started

This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

## Prerequisites

Before running the project, ensure you have the following installed:

- [Node.js](https://nodejs.org/en/)

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/nishkarsh25/NEXTJS-TicketApp.git
   ```
2. Navigate to the project branch:

   ```bash
   git checkout <branch-name>
   ```
   Replace `<branch-name>` with the name of the branch you want to checkout.
   

3. Run the development server:

    ```bash
    npm run dev
    # or
    yarn dev
    # or
    pnpm dev
    # or
    bun dev
    ```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.js`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

## How to Use

### Creating a Ticket

1. **Navigate to the Dashboard**: Open the dashboard page where you can see the list of all tickets.
2. **Click "Create New Ticket"**: This will open a form to create a new ticket.
3. **Fill in the Form**:
   - **Title**: Enter the ticket's title.
   - **Description**: Provide detailed information about the issue.
   - **Category**: Select a category from the dropdown (e.g., Hardware Problem, Software Problem, Application Development, Project).
   - **Priority**: Choose a priority level from 1 (lowest) to 5 (highest).
   - **Progress**: Use the slider to set the progress percentage.
   - **Status**: Select the current status (Not Started, Started, Done).
4. **Submit the Form**: Click "Create Ticket" to save the new ticket.

### Viewing Tickets

- **Dashboard View**: Tickets are displayed on the dashboard, categorized by their category.
- **Detailed View**: Click on a ticket title to view more details about that ticket, including its progress, priority, and status.

### Updating a Ticket

1. **Select a Ticket**: Click on the ticket you want to update.
2. **Edit the Fields**: Modify the necessary fields in the form.
3. **Save Changes**: Click "Update Ticket" to save your changes.

### Deleting a Ticket

- **Delete Icon**: Click the delete icon (X) on the ticket card.
- **Confirm Deletion**: Confirm the deletion if prompted. The ticket will be removed from the list.


## API Endpoints

### GET /api/Tickets

- **Description**: Fetches all tickets from the database.
- **Method**: GET
- **Response**: 
  - **Status**: 200 OK
  - **Body**: JSON object containing an array of ticket objects.

### POST /api/Tickets

- **Description**: Creates a new ticket in the database.
- **Method**: POST
- **Request Body**: 
  - **Content Type**: application/json
  - **Format**: JSON object containing ticket data.
- **Response**: 
  - **Status**: 201 Created or 500 Internal Server Error
  - **Body**: JSON object containing a message indicating success or failure.

### GET /api/Tickets/:id

- **Description**: Fetches a specific ticket by its ID.
- **Method**: GET
- **Parameters**: 
  - **id**: ID of the ticket to fetch.
- **Response**: 
  - **Status**: 200 OK or 404 Not Found
  - **Body**: JSON object containing the ticket data or an error message.

### PUT /api/Tickets/:id

- **Description**: Updates an existing ticket by its ID.
- **Method**: PUT
- **Parameters**: 
  - **id**: ID of the ticket to update.
- **Request Body**: 
  - **Content Type**: application/json
  - **Format**: JSON object containing updated ticket data.
- **Response**: 
  - **Status**: 200 OK or 500 Internal Server Error
  - **Body**: JSON object containing a message indicating success or failure.

### DELETE /api/Tickets/:id

- **Description**: Deletes a specific ticket by its ID.
- **Method**: DELETE
- **Parameters**: 
  - **id**: ID of the ticket to delete.
- **Response**: 
  - **Status**: 200 OK or 500 Internal Server Error
  - **Body**: JSON object containing a message indicating success or failure.


## Contributing

Contributions to this project are highly appreciated! Whether you discover bugs, have feature requests, or wish to contribute improvements, your input is valuable. Here's how you can contribute:

- **Report Issues:** If you encounter any bugs or issues while using MyCalculatorApp, please open an issue on the GitHub repository. Be sure to provide detailed information about the problem and steps to reproduce it.

- **Submit Pull Requests:** If you have enhancements or fixes to propose, feel free to submit a pull request. Contributions that improve the functionality, usability, or performance of this app are welcomed and encouraged.

Contributions are welcome! If you'd like to contribute to this project, please follow these steps:

1. **Fork the Repository**.
2. **Create a New Branch** (`git checkout -b feature/your-feature-name`).
3. **Make Your Changes**.
4. **Commit Your Changes** (`git commit -am 'Add some feature'`).
5. **Push to the Branch** (`git push origin feature/your-feature-name`).
6. **Create a New Pull Request**.

## License

This project is licensed under the [The 3-Clause BSD License](LICENSE).Feel free to explore, modify, and contribute to this project as you see fit. Your feedback and contributions are greatly appreciated! 🚀✨


## Acknowledgments

This project is made possible by the contributions and support of various individuals and communities. Special thanks to:

- **Tailwind CSS Team:** For developing Tailwind CSS, a versatile CSS framework that simplifies web development and enhances user interfaces.
  
- **Open Source Community:** For fostering collaboration, innovation, and the sharing of knowledge, which enriches projects like My Form Validation and makes them accessible to all.


## Credits

This project wouldn't be possible without the contributions of the following:

- **Next.js**: Next.js is a React framework that enables functionality such as server-side rendering and generating static websites for React-based web applications. Visit [Next.js](https://nextjs.org/) for more information.

- **React**: A JavaScript library for building user interfaces. Visit [React](https://reactjs.org/) for more information.

- **React Icons**: React Icons provides a comprehensive library of icons for React applications. Visit [React Icons](https://react-icons.github.io/react-icons/) for more information.
  
- **Tailwind CSS**: A utility-first CSS framework for creating custom designs rapidly. Visit [Tailwind CSS](https://tailwindcss.com/) for more information.

- **FontAwesome**: A popular icon library providing a vast collection of icons for web development. Visit [FontAwesome](https://fontawesome.com/) for more information.

- **React Router**: React Router is a library for routing in React applications, allowing for navigation between different components. Visit [React Router](https://reactrouter.com/) for more information.

- **Axios**: Axios is a promise-based HTTP client for making asynchronous requests in JavaScript applications. Visit [Axios](https://axios-http.com/) for more information.

- **Mongoose**: Mongoose is an Object Data Modeling (ODM) library for MongoDB and Node.js, providing a straightforward schema-based solution for modeling application data. Visit [Mongoose](https://mongoosejs.com/) for more information.

- **Node Mailer**: Nodemailer is a module for Node.js applications that allows sending emails. It is a powerful and easy-to-use module for sending email using Node.js. Visit [Nodemailer](https://nodemailer.com/about/) for more information.

- **Netlify**: Netlify provides seamless deployment and hosting solutions, making it easy to deploy web applications and share them with the world. Visit [Netlify](https://www.netlify.com/) for more information.

- **Render**: Render offers a modern cloud platform for deploying and running web applications, databases, and other services. Visit [Render](https://render.com/) for more information.

- **MongoDB Atlas**: MongoDB Atlas is a fully managed cloud database service for modern applications. Visit [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) for more information


## Author

- **Nishkarsh Gupta**
  - GitHub: [nishkarsh25](https://github.com/nishkash25)
  - Email: bm21btech11016@gmail.com



