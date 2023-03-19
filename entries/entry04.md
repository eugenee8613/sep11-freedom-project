# Entry 4
##### 3/19/23

Me and my parnter Josiah have been looking over and tinkering  with some of the  code that we have learned from the tutorial. We  have been  making the outline for our MVP.  We have been working on specifically some code that will effectively take data from the realtime database nodes and then use that data output onto  the screen and do other things like adding it into variables.



So as I was saying this code reads data from the Firebase Realtime Database in the workouts node using a once() method. It then loops through each child snapshot of the workouts node and retrieves the name and description values of each workout using the val() method. The name and description values are then concatenated into an HTML string which is added to the workoutPlanner variable. Finally, the innerHTML property of the workout-planner element is set to the workoutPlanner variable, which will display the retrieved workout data on the webpage. Although Firebase is really challenging we have been taking bits and pieces from research and tutorials to put together pieces of our MVP and this is one of them.


Example
```
database.ref('workouts').once('value').then(function(snapshot){
    var  workoutPlanner = '';
    snapshot.forEach(function(childSnapshot)){
        var workout = childSnapshot.val();
        workoutPlanner += '<div><h2>' + workout.name + '</h2><p>' + workout.description + '</p></div>';
    });
    document.getElementById('workout-planner').innerHTML = workoutPlanner;



Engineering Design Process
    Me and my partner are up to stage 4 of the EDP which is Plan the most promising solution because I am planning the best and most efficient way to meet my MVP. I am using research I already did and I am using that to go forward in the EDP and start planning and carrying out pieces of the plan.


Skills
    Me and my partner are using the skills How to google, How to learn, and How to read. We are  using these skills by taking information of different places and reading documentations then putting it into the code and changing it to fit our needs and making it do for the requirements of our MVP.


[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)