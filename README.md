# Glue42 Angular Example

This is a simple Angular project, which showcases Glue42 Desktop initiation and integration in a standard Angular application. This project was generated with the standard Angular CLI version 1.4.9, using default settings. The project structure and organization is not modified in any way.

## Initiating the Angular Example

1. Clone the repository.
2. Install the dependencies by `npm install`.
3. Paste the `angular-example.json` file in the `%localappdata%/Tick42/GlueDesktop/config/apps` folder.
4. Run the example project with the command `npm run serve`. The application will run at the default ng port 4200.
5. Start Glue42 Desktop and select the application from the dropdown menu of the Application Manager on the Glue42 Desktop Toolbar.

## Glue42 Initiation and Usage

**Initiation**

The `glue.js` library initiation is asynchronous. It is declared in `src/app/glue/glue.service.ts`. Since our entire app logic depends on Glue42, we used the `APP_INITIALIZER` to extend the Angular example default bootstrap procedure. If the initiation is successful, you should see the loaded `glue.js` version on the home screen. 

**Usage**

The `GlueService`, declared in `src/app/glue/glue.service.ts`, initializes and provides access to the `glue` object. It is recommended that the `glue` object remains encapsulated and only the needed functionality is exposed, like the example `register()` method. Alternatively, this service could expose the entire `glue` object or some selected libraries, like the `interop` property.

A sample Interop method registration is shown in `src/app/app.component.ts`, where all three options described above are used.