## Endurance Data
  *The newest fitness tracking tool*




#### Deployment:

  App is deployed at: https://endurancedata.netlify.com/ 




#### Description:

  Endurance Data is a cloud-based workout log.  Endurance data is designed for use by endurance athletes (runners and cyclists).  This app has an easy-to-use interface, and is capable of tracking all of an athlete's training data.  Users enter data from their workouts manually, and Endurance Data will store and display this data.

  Endurance Data is unique to each user because each user can choose what data he/she wants to log.  For example, a beginning runner might only want to track their total mileage for each day.  This user will receive a user-interface that is simplified to only include this input field.  However, a professional cyclist might want to keep track of Total Time, Average Heartrate, Max Heartrate, Average Watts, Max Watts, Hours of Sleep, Soreness Rating, Time Spent Stretching, etc. for each day.  This user would have an interface where each of these input fields is brought up by default.  Endurance Data stores each workout in a database, and allows users to recall their workouts.

  ...*Feature Coming Soon*...Endurance data will allow a user to perform an analysis of their data.  For example, a user might selete to see *"Miles per day over the past week"*, and Endurance Data would display *"You averaged 5.2 miles per day over the past week"*.  This feature is still in production, and the app works perfectly fine without it for now.



#### Screenshots:

#### Description of Tech Stack:

   Endurance Data is created using React for the front-end and Node.js for the back-end.

   *Front-end:* The clientside of this app is created using React.  Redux is used to manage the high-level state of the app.  React Stateful components are used to manage the state that is specific to each component.  `react-router-dom` is used to route users to different components based on their url path.  `moment.js` is used to format dates and perform calculations with the dates.  `enzyme` is used to test each component.  As of now, each component is tested, but many tests are just smoke tests.  API calls are made using Javascript's `fetch` method.  The server-side is located in a separate repo.

   *Back-end:* Here is the [server-side repo](https://github.com/thinkful-ei22/morgan-fullStack-server.git) for this application.  The server-side is written in `Node.js` and uses `express` to route incoming requests.  The app uses a MongoDB to store the data, which is hosted by mLab.com.  The server-side uses `bcryptjs` to encrypt user passwords for maximum security.  The server-side also uses the `jsonwebtoken` library to issue webtokens to users, which is stored in local storage on the front-end.  The server-side uses `mongoose` as the query library when making calls to the database.  Server-side tests are written using the `mocha` and `chai` libraries, with `chai-http` to simulate requests to the server.  The back-end is published live using [heroku](https://endurance-data-server.herokuapp.com/).

#### Description of Key Code Snippets:
