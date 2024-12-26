Prerequisites:

    Install Flask: 
      pip install flask

    Run the Server:
      python <script_name>.py

Functionalities:

    Add a New Student (POST /students):
        Expects a JSON payload containing student details including id.
        Adds the student to the students dictionary.

    Get All Students (GET /students):
        Returns a list of all student records.

    Get a Student with an ID (GET /students/<id>):
        Retrieves a specific student by their id.

    Update Existing Student (PUT /students/<id>):
        Updates details of an existing student.

    Delete a Student Record (DELETE /students/<id>):
        Removes a student record from the students dictionary.
        
Example Test Commands:

  Add Student:

      curl -X POST -H "Content-Type: application/json" -d '{"id": 1, "name": "John", "grade": "A"}' http://127.0.0.1:5000/students

  Get All Students:

      curl http://127.0.0.1:5000/students

  Update Student:

      curl -X PUT -H "Content-Type: application/json" -d '{"grade": "A+"}' http://127.0.0.1:5000/students/1

  Delete Student:

      curl -X DELETE http://127.0.0.1:5000/students/1
