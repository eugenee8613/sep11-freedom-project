# Entry 2: Learning 
 12/17/22

   I have been learning my tool by watching youtube videos. I started watching this channel called Net Ninja. Also for this project I am working with my partner Josiah. We are working together on firebase and trying something new and we want to challenge our selves. So far we watched only 3 out of 9 videos we are going slow and step by step so we don't mess up and so we can actually undertand what to do.

```
// First, you need to add the Firebase Realtime Database to your project:
implementation 'com.google.firebase:firebase-database:19.3.1'

// Then, you can use the following code to write data to the database:
FirebaseDatabase database = FirebaseDatabase.getInstance();
DatabaseReference myRef = database.getReference("message");

myRef.setValue("Hello, World!");

// You can also use the following code to read data from the database:
myRef.addValueEventListener(new ValueEventListener() {
  @Override
  public void onDataChange(DataSnapshot dataSnapshot) {
    // This method is called once with the initial value and again
    // whenever data at this location is updated.
    String value = dataSnapshot.getValue(String.class);
    Log.d(TAG, "Value is: " + value);
  }

  @Override
  public void onCancelled(DatabaseError error) {
    // Failed to read value
    Log.w(TAG, "Failed to read value.", error.toException());
  }
});
```
This code creates a reference to the "message" node in the database, and then writes the string "Hello, World!" to that node. It also sets up a listener that will be called whenever the data at that location is updated.  My goal for this winter break is to try to focus on understanding what firebase is and slowy proceeding to make it able to be used in real life. Before I go to Pennsylvania I will create a timeline for myself so I can be on task. Once I come back I will be doing those tasks so I will stay up to date. On the EDP me and my parnter are up to the research part because we are still watching videos on how to firebase works. I am using the skill how to google by searching up how firebase works and how to start it.
