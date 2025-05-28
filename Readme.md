### Step 1: First Command to run:
- mongosh "mongodb+srv://cluster0.loewrvf.mongodb.net/" --apiVersion 1 --username omraj

### Step 2: Code to create todo list:
- use todo_db

### Step 3: Code to write 1 todo list:
- db.tasks.insertOne({description: "Buy Shoes", status: "pending", created_at: new Date()})
- _id: ObjectId('6836e2afc7996ce8cc6c4bd0')
- description : "Buy Shoes"
- status : "pending"
- created_at : 2025-05-28T10:17:19.273+00:00