## todo list creation:

### Step 1: First Command to run:
- mongosh "mongodb+srv://cluster0.loewrvf.mongodb.net/" --apiVersion 1 --username omraj

### Step 2: Code to create todo list:
- use todo_db

### Step 3: Code to write 1 todo list:
- db.tasks.insertOne({description: "Buy Shoes", status: "pending", created_at: new Date()})
- _id: ObjectId('6836e2afc7996ce8cc6c4bd0')  
  description : "Buy Shoes"  
  status : "pending"  
  created_at : 2025-05-28T10:17:19.273+00:00

### Step 3: Code to write 10 todo list:
- db.tasks.insertMany(  
  { description: "complete homework", status: "pending", created_at: new Date() },  
  { description: "Call mom", status: "pending", created_at: new Date() },  
  { description: "Finish reading book", status: "pending", created_at: new Date() },  
  { description: "Reply to emails", status: "pending", created_at: new Date() },  
  { description: "Clean the room", status: "pending", created_at: new Date() },  
  { description: "Water the plants", status: "pending", created_at: new Date() },  
  { description: "Exercise for 30 minutes", status: "pending", created_at: new Date() },  
  { description: "Plan the weekend trip", status: "pending", created_at: new Date() },  
  { description: "Review project notes", status: "pending", created_at: new Date() }  
)