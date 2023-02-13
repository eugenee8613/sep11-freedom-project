# Entry 3
##### 2/11/23

So right me and my parnter are cunrrently up to the research part of the Engineering Design Process. Our tool that we are using is called firebase. So what is firebase you might be asking. Firebase is a mobile and web application development platform that provides a variety of tools and services to help developers build high-quality, scalable, and real-time applications. It was acquired by Google in 2014 and has since then become one of the most popular back-end as a service (BaaS) platforms available.
Firebase provides several key features, including, Real-time Database: A NoSQL database that allows for real-time data synchronization across connected clients, Cloud Firestore: A scalable, cloud-native NoSQL document database for web and mobile app development. Authentication: An authentication system that supports various authentication methods, including email/password, phone number, and third-party providers like Google, Facebook, and more. Cloud Functions: A serverless platform for creating and running backend code. Hosting: A static and dynamic web hosting service Storage: A scalable and secure cloud-based object storage service. Machine Learning: A set of machine learning APIs for natural language processing, image analysis, and more. Firebase is often used in the development of modern web and mobile applications because it provides a comprehensive set of services and features that help simplify the development process and allow developers to focus on building the core functionality of their app. Additionally, Firebase integrates well with other Google products and services, making it a popular choice for developers working with Google's ecosystem. Me and and my partner are researching by going on slack and using the fcc. Here is some code that we have already utilized. We are trying to make a workout planner/maker for users.

``/Function to retieve the workout history
function  getWorkoutHistory(){
  database.ref("workouts").on("value", function(snapshot){
    console.log(snapshot.val));
  });

}
//Example
logWorkout({
    type: "Chest"
    date: "2023-02-12"
    sets: 3,
    reps: 10,
})
getWorkoutHistory();
``

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
