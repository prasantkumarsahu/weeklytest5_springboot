# Job Management System
This is a API project for insert, read, update, and delete Jobs using **H2 Database** and `CrudRepository`.

![Spring Boot](https://img.shields.io/badge/Spring_Boot-F2F4F9?style=for-the-badge&logo=spring-boot "Spring Boot") ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white "Java") ![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white "Postman") ![Google Chrome](https://img.shields.io/badge/Google%20Chrome-4285F4?style=for-the-badge&logo=GoogleChrome&logoColor=white "Google Chrome")

## Frameworks and Languages
![Java v17](https://img.shields.io/badge/Java-v17-green "Java 17") ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-v3.0.5-brightgreen "Spring Boot v3.0.5")

---
## Browser / Tools
![Google Chrome](https://img.shields.io/badge/Google%20Chrome-v112.0.5615.138-yellow "Google Chrome") ![Postman](https://img.shields.io/badge/Postman-v10.13.0-orange "Postman")
---

## Model
- ### User Properties
    - ```java
      private int userId;
      ```
    - ```java
      @NotBlank
      private String userName;
      ```
    - ```java
      @Pattern(regexp = "[0-9]{2}-[0-9]{2}-[0-9]{4}", message = "Enter a valid date (DD-MM-YYYY)")
      private String dateOfBirth;
      ```
    - ```java
      @Email
      private String email;
      ```
    - ```java
      @Pattern(regexp = "[0-9]{12}", message = "Phone number must be contains 12 digits!")
      private String phoneNumber;
      ```
    - ```java
      @Pattern(regexp = "[0-9]{2}-[0-9]{2}-[0-9]{4}", message = "Enter a valid date (DD-MM-YYYY)")
      private String date;
      ```
    - ```java
      @Pattern(regexp = "[0-9]{2}:[0-9]{2}", message = "Enter a valid time (HH:MM)")
      private String time;
      ```
---
## Dataflow
- ### End Points / Controllers
    - `addUser` 
    - `getUser/{userId}`
    - `getAllUser`
    - `updateUserInfo/{userId}`
    - `deleteUser/{userId}`
- ### Services
    - For adding user
        ```java
        public String addUser(User newUser)
        ```
    - For getting user based on Id
        ```java
        public User getUserById(int userId)
        ```
    - For getting all the users
        ```java
        public List<User> getAllUsers() 
        ```
    - For updating user info
        ```java
        public String updateUser(User updatedUser) 
        ```
    - For deleting an user
        ```java
        public List<User> getAllUsers() 
        ```
- ### Repository
    - Getting all the users from data source
        ```java
        public List<User> getAllUsersFromDataSource()
        ```
    - Saving the user into the data source
        ```java
        public boolean insertUser(User newUser)
        ```
    - Removing user from the data source
        ```java
        public void remove(User user)
        ```
- ### Database
I haven't used any **Database** in this project yet. But for data storing I have used an `Collections`.

```java
private List<User> userList;
```
---
## Datastructures
- `ArrayList<>`
---
## Summary
This API is a `Spring Boot` project that is about managing users. We can create, read, update, and delete user. In this project request is sent from the client on HTTP in JSON format or from path variable with server side validations and stored in object then response is sent back from the server by JSON format to the client.
