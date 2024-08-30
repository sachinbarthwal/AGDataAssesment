# Address Management Application

This project consists of an Angular frontend and a .NET Core backend API with RavenDB integration.

## Prerequisites

- Node.js (v14 or later)
- .NET Core SDK 6.0
- Angular CLI (v15)
- RavenDB Server

## RavenDB Setup

1. Download and install RavenDB from https://ravendb.net/download
2. Start the RavenDB server
3. The application is configured to connect to RavenDB at http://localhost:8080. If your RavenDB is running on a different URL, update the `appsettings.json` file in the AddressAPI project accordingly.
4. :warning: **Please make sure RavenDb is installed with AddressDb database else this application will fail**

## Setup Instructions

1. Clone the repository:
git clone https://github.com/sachinbarthwal/AGDataAssesment.git
cd AGDataAssesment

2. Set up the backend:
cd AddressAPI
dotnet restore
dotnet build


3. Set up the frontend:
cd ../AngularFrontend
npm install
npm install bootstrap

4. Run the application:
- Start the backend:
  ```
  cd ../AddressAPI
  dotnet run
  ```
- In a new terminal, start the frontend:
  ```
  cd ../AngularFrontend
  ng serve
  ```

5. Open a web browser and navigate to `http://localhost:4200`

## Running the Application

- The backend API will be available at `https://localhost:7262`
- The frontend will be served at `http://localhost:4200`

## Project Structure

- `AddressAPI/`: .NET Core 6 backend with RavenDB integration
- `AngularFrontend/`: Angular 15 frontend application

## Backend (AddressAPI)

- Built with .NET Core 6
- Uses RavenDB for data persistence
- Implements RESTful API endpoints for address management

## Frontend (AngularFrontend)

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 15.0.3.

### Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

### Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

### Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

### Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

### Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Troubleshooting

- If you encounter CORS issues, ensure that the backend is properly configured to allow requests from the frontend origin.
- Verify that RavenDB is running and accessible at the configured URL before starting the backend.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.

For backend issues, refer to the .NET Core and RavenDB documentation.
