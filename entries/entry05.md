# Entry 5
##### 4/23/23
 I had the opportunity to learn Firebase, a powerful and flexible backend-as-a-service (BaaS) platform that allowed me to easily incorporate real-time data synchronization and authentication into my web applications. One of the projects I worked on was building a workout planner using Firebase, and I am excited to share my journey and the process of building a Minimum Viable Product (MVP) for my workout planner using Firebase.

Our firebase code:
```<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Workout Planner</title>
  </head>
  <body>
    <div id="header">
      <h1>Workout Planner</h1>
      <p id="user-profile"></p>
    </div>
    <form id="workout-form">
      <label>
        <input type="checkbox" name="upper-body"> Upper Body
      </label>
      <label>
        <input type="checkbox" name="lower-body"> Lower Body
      </label>
      <label>
        <input type="checkbox" name="cardio"> Cardio
      </label>
      <button type="submit">Generate Workout</button>
    </form>
    <div id="workout-planner"></div>
    <script src="https://www.gstatic.com/firebasejs/8.2.1/firebase-app.js"></script>
    <script src="https://www.gstatic.com/firebasejs/8.2.1/firebase-auth.js"></script>
    <script src="https://www.gstatic.com/firebasejs/8.2.1/firebase-database.js"></script>
    <script>
      // Initialize Firebase



      var config = {
      apiKey: "AIzaSyDyW_L7Arqow6M9ztcCmlMde-glmad7Rh4",
      authDomain: "chicken-a44ee.firebaseapp.com",
      databaseURL: "https://chicken-a44ee-default-rtdb.firebaseio.com/",
      projectId: "chicken-a44ee",
      storageBucket: "chicken-a44ee.appspot.com",
      messagingSenderId: "861457030837"
    };
    firebase.initializeApp(config);

      var firebaseConfig = {
        // Your Firebase project configuration
      };
      firebase.initializeApp(firebaseConfig);

      // Get a reference to the database service
      var database = firebase.database();

      document.getElementById('workout-form').addEventListener('submit', function(event) {
        event.preventDefault();
        generateWorkout();
      });

      function generateWorkout() {
        // Get user preferences
        var preferences = {};
        var checkboxes = document.querySelectorAll('#workout-form input[type="checkbox"]');
        checkboxes.forEach(function(checkbox) {
          preferences[checkbox.name] = checkbox.checked;
        });

        // Query database for matching workouts
        database.ref('workouts').orderByChild('type').equalTo(true).once('value').then(function(snapshot) {
          var workoutPlanner = '';
          snapshot.forEach(function(childSnapshot) {
            var workout = childSnapshot.val();
            // Add logic to filter workouts based on user preferences
            // and append the generated workout to the workoutPlanner div
          });
          document.getElementById('workout-planner').innerHTML = workoutPlanner;
        });
      }
    </script>
  </
  ```


To get started, I included the Firebase JavaScript libraries in my HTML file using the CDN links for Firebase App, Firebase Auth, and Firebase Database. I also initialized Firebase with my project's configuration by providing the necessary API key, authentication domain, database URL, project ID, storage bucket, and messaging sender ID. This allowed me to establish a connection between my web application and the Firebase backend.

Next, I created a simple HTML form with checkboxes for the user to select their workout preferences, such as upper body, lower body, and cardio exercises. I also added a submit button to trigger the generation of a workout based on the user's preferences. I attached an event listener to the form's submit event and called the generateWorkout() function to handle the logic for generating the workout.

In the generateWorkout() function, I first retrieved the user's preferences by querying the checkboxes and storing the values in an object called preferences. Then, I used Firebase's Realtime Database to query for workouts that matched the user's preferences. I used the orderByChild() and equalTo() methods to filter the workouts based on the 'type' field in my Firebase database, which represented the different workout types (upper body, lower body, and cardio). I used the once() method to retrieve the data from the database as a snapshot, and then iterated through the snapshot to extract the workout data.

At this point, I was able to append the generated workout to the workout planner div in my HTML file. However, I needed to add additional logic to filter the workouts based on the user's preferences before appending them to the DOM. For example, I could check if the workout type matched any of the user-selected preferences, and only append the workout if it did. I could also add additional logic to randomize the selection of workouts or limit the number of workouts generated based on the user's preferences.

Overall, Firebase made it easy for me to incorporate real-time data synchronization and authentication into my workout planner project. The ability to query and retrieve data from the Firebase Realtime Database in real-time was particularly powerful, allowing me to build dynamic and responsive web applications. Firebase also provided built-in authentication functionality, which I could have leveraged to authenticate users and store user-specific data, such as workout history or user preferences, in Firebase's NoSQL database.

In conclusion, learning Firebase in my software engineering class was a valuable experience. Building a workout planner using Firebase allowed me to practice working with real-time data synchronization, querying data from a NoSQL database, and integrating authentication functionality into my web application. I am excited to continue exploring Firebase and leveraging its capabilities in future projects, and I highly recommend it as a powerful backend-as-a-service platform for web development projects.
[Previous](entry04.md) | [Next](entry06.md)



[Home](../README.md)