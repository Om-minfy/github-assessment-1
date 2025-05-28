## todo list creation:

### Step 1: First Command to run:
- mongosh "mongodb+srv://cluster0.loewrvf.mongodb.net/" --apiVersion 1 --username omraj

### Step 2: Code to create todo list:
- use todo_db

### Step 3: Code to write 1 todo list:
- db.tasks.insertOne(  
  { description: "Buy Shoes", status: "pending", created_at: new Date()}  
)
- _id: ObjectId('6836e2afc7996ce8cc6c4bd0')  
  description : "Buy Shoes"  
  status : "pending"  
  created_at : 2025-05-28T10:17:19.273+00:00

### Step 4: Code to write 10 todo list:
- db.tasks.insertMany(  
  { description: "Buy groceries", status: "pending", created_at: new Date() },  
  { description: "Complete homework", status: "pending", created_at: new Date() },  
  { description: "Call mom", status: "pending", created_at: new Date() },  
  { description: "Finish reading book", status: "pending", created_at: new Date() },  
  { description: "Reply to emails", status: "pending", created_at: new Date() },  
  { description: "Clean the room", status: "pending", created_at: new Date() },  
  { description: "Water the plants", status: "pending", created_at: new Date() },  
  { description: "Exercise for 30 minutes", status: "pending", created_at: new Date() },  
  { description: "Plan the weekend trip", status: "pending", created_at: new Date() },  
  { description: "Review project notes", status: "pending", created_at: new Date() }  
)
- _id: ObjectId('6836e3f9c7996ce8cc6c4bd1')  
description: "Buy groceries"  
status: "pending"  
created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd2')  
  description: "Complete homework"  
  status: "pending"  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd3')  
  description: "Call mom"  
  status: "pending"  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd4')  
  description: "Finish reading book"  
  status: "pending"  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd5')  
  description: "Reply to emails"  
  status: "pending"  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd6')  
  description: "Clean the room"  
  status: "pending"  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd7')  
  description: "Water the plants"  
  status: "pending"  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd8')  
  description: "Exercise for 30 minutes"  
  status: "pending"  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd9')  
  description: "Plan the weekend trip"  
  status: "pending"  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bda')  
  description: "Review project notes"  
  status: "pending"  
  created_at: 2025-05-28T10:22:49.890+00:00

### Step 5: View all tasks:
- db.tasks.find()

### Step 6: Convert status Field to Boolean:
- db.tasks.updateMany(  
  { status: "pending" },  
  { $set: { status: false } }  
)
- _id: ObjectId('6836e2afc7996ce8cc6c4bd0')  
  description : "Buy Shoes"  
  status : false  
  created_at : 2025-05-28T10:17:19.273+00:00

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd1')  
  description: "Buy groceries"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd2')  
  description: "Complete homework"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd3')  
  description: "Call mom"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd4')  
  description: "Finish reading book"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd5')  
  description: "Reply to emails"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd6')  
  description: "Clean the room"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd7')  
  description: "Water the plants"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd8')  
  description: "Exercise for 30 minutes"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd9')  
  description: "Plan the weekend trip"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bda')  
  description: "Review project notes"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00

### Step 7: Status should be false by default:
- db.tasks.insertOne({  
    description: "New task from user",  
    status: false,  
    created_at: new Date()  
})

### Step 8: Update the status field from false to true for a specific task:
- db.tasks.updateOne(  
  { _id: ObjectId('6836e3f9c7996ce8cc6c4bd2') },  
  { $set: { status: true } }  
)
- _id: ObjectId('6836e2afc7996ce8cc6c4bd0')  
  description : "Buy Shoes"  
  status : false  
  created_at : 2025-05-28T10:17:19.273+00:00

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd1')  
  description: "Buy groceries"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd2')  
  description: "Complete homework"  
  status: true  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd3')  
  description: "Call mom"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd4')  
  description: "Finish reading book"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd5')  
  description: "Reply to emails"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd6')  
  description: "Clean the room"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd7')  
  description: "Water the plants"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd8')  
  description: "Exercise for 30 minutes"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bd9')  
  description: "Plan the weekend trip"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00  

  _id: ObjectId('6836e3f9c7996ce8cc6c4bda')  
  description: "Review project notes"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00

### Step 9: Verify the update:
- db.tasks.find({ _id: ObjectId('6836e3f9c7996ce8cc6c4bd2') })

### Step 10: Update any task in MongoDB and automatically set an updated_at timestamp:
- db.tasks.updateOne(  
  { _id: ObjectId('6836e3f9c7996ce8cc6c4bd3') },  
  { $set: {  
      description: "Buy groceries and fruits",  
      status: false,  
      updated_at: new Date()  
    } }  
)
- _id: ObjectId('6836e3f9c7996ce8cc6c4bd3')  
  description: "Buy groceries and fruits"  
  status: false  
  created_at: 2025-05-28T10:22:49.890+00:00  
  updated_at: 2025-05-28T10:41:39.890+00:00