---
sidebar_position: 3
---

dotwise frontend Documentation
=============================


Installation
------------

1.  Clone the repository:  
    `git clone https://github.com/your-username/dotwise.git`
2.  Navigate to the project directory:  
    `cd dotwise`
3.  Install dependencies:  
    `npm install`

Environment Variables
---------------------

Create a `.env` file in the root directory of your project and add the following variables:

    VITE_LRT_OR_RTL=rtl

Routes Component
================

The Routes component handles the routing and navigation within the application using React Router. It defines different routes and their corresponding components to be rendered based on the current URL.


Explanation
-----------

The Routes component is a functional component that uses React Router to handle navigation. It sets up the routing configuration by defining the routes and their corresponding components to be rendered based on the current URL.

The component uses the BrowserRouter component from react-router-dom as the router wrapper. Inside the BrowserRouter, it renders the ScrollToTop component, HeaderContainer component, Switch component, Footer component, GetContent component, and MediaRunningContainer component (depending on the browser type).

The Switch component renders the routes defined in the publicPages and privatePages arrays using the Route component. It also handles the rendering of the Page404 component for any unknown routes.

The PrivateRoute component is a custom component that allows rendering of private routes only when the user is authenticated. It redirects the user to the login page if they are not authenticated.

The Routes component also includes logic to handle public pages and public pages only. Public pages are rendered when the user is not authenticated, while public pages only are rendered when the user is authenticated (to prevent accessing these pages when already logged in).

Running the Project
-------------------

To start the development server, run the following command:

    npm run dev

The application will be accessible at [http://localhost:3000](http://localhost:3000).

Building the Project
--------------------

To build the project for production, run the following command:

    npm run build

The optimized and minified files will be available in the `dist` directory.

Deploying the Project
---------------------

You can deploy the built files to a static hosting service of your choice. Here are some common deployment options:

*   Netlify: [Netlify Docs](https://docs.netlify.com/)
*   Vercel: [Vercel Docs](https://vercel.com/docs)
*   GitHub Pages: [GitHub Pages Docs](https://docs.github.com/en/pages)

Choose the deployment method that suits your requirements and follow the respective documentation.


Entry Point
-----------

The main entry point of the project is `src/index.tsx`.

