package main2;

class User {
    String username;
    String password;

    void login() {
        System.out.println(username + " logged in.");
    }
}

class Student extends User {
    String studentId;

    void registerCourse(String courseName) {
        System.out.println("Student " + username + " registered for course: " + courseName);
    }
}

public class assign3 {
    public static void main(String[] args) {
        Student student = new Student();
        student.username = "john_doe";
        student.password = "securepassword"; // inherited from User
        student.studentId = "S12345";

        student.login(); // reused method from User class
        student.registerCourse("Computer Science 101");
    }
}