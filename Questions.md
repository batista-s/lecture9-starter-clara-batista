**The Hidden ID:** In your magazine-form.html, you included <input type="hidden" th:field="*{id}" />. What would happen if you forgot to include this line, and a user tried to "Edit" an existing magazine? Why?

**The PRG Pattern:** Why does our save method return "redirect:/magazines" instead of just returning the "magazine-list" HTML template directly?

**Data Binding:** What is the purpose of the @ModelAttribute annotation in your @PostMapping method? What manual work does it save you from doing?

**Fragments:** You used th:replace="~{fragments/navbar :: header}" on multiple pages. What is the primary benefit of this approach in a real-world application with 50+ HTML pages?

Lab 7: 20 Multiple Choice Questions
I will take up the questions in a later lecture.
1. What does "SSR" stand for in the context of our Spring Boot application?
   <br> A. Simple Server Routing
   <br> B. Server-Side Rendering
   <br> C. Spring Security Rules
   <br> D. Static System Resources
2. Which Spring MVC annotation is used to mark a class that returns HTML template names instead of raw JSON data?
   <br> A. @RestController
   <br> B. @Service
   <br> C. @Controller
   <br> D. @Repository
3. In the URL http://localhost:8080/magazines/edit/5, what annotation is used to extract the number 5 in the Java Controller?
   <br> A. @RequestParam
   <br> B. @PathVariable
   <br> C. @ModelAttribute
   <br> D. @Mapping
4. What is the primary role of Thymeleaf in our application?
   <br> A. To act as the database.
   <br> B. To intercept HTTP requests before the Controller.
   <br> C. To stitch dynamic Java data into static HTML templates before sending it to the browser.
   <br> D. To generate CSS styles automatically.
5. If a user submits an HTML <form method="post">, which annotation should the receiving method in the Controller use?
   <br> A. @GetMapping
   <br> B. @PutMapping
   <br> C. @PostMapping
   <br> D. @RequestMapping
6. What does the Thymeleaf attribute th:each="mag : ${magazines}" do?
   <br> A. It deletes all magazines.
   <br> B. It loops over a list called "magazines" passed from the Model, generating a new HTML element for each item.
   <br> C. It counts the number of magazines in the database.
   <br> D. It searches for a specific magazine by I<br> D.
7. Why do we need a specific MagazineRepository if we already have a ProductRepository?
   <br> A. Because ProductRepository cannot connect to MySQL.
   <br> B. To allow Spring Data JPA to access subclass-specific fields like publisher that the parent ProductEntity does not have.
   <br> C. Because you can only save one entity per repository.
   <br> D. To make the application run faster.
8. In Spring MVC, what is the "Model"?
   <br> A. The database server.
   <br> B. The Thymeleaf HTML file.
   <br> C. A "suitcase" object used to pass data from the Java Controller to the HTML View.
   <br> D. The URL path of the application.
9. What does the redirect:/ prefix do when returned by a Controller method?
   <br> A. It crashes the application.
   <br> B. It renders an HTML page called "redirect".
   <br> C. It tells the user's browser to make a brand new GET request to the specified URL.
   <br> D. It encrypts the user's session.
10. What HTTP request type is considered unsafe for saving sensitive data because the data is visible in the URL?
    <br> A. POST
    <br> B. GET
    <br> C. PUT
    <br> D. DELETE
11. What does the @ModelAttribute("magazine") MagazineEntity mag annotation do?
    <br> A. It connects to the database to find a magazine.
    <br> B. It automatically takes submitted HTML form fields and binds them to a new Java object.
    <br> C. It creates a new HTML file.
    <br> D. It authenticates the user.
12. If you call magazineRepository.save(mag) and the mag.getId() is currently null, what does Spring Data JPA do?
    <br> A. It throws a NullPointerException.
    <br> B. It performs an SQL UPDATE on row 0.
    <br> C. It performs an SQL INSERT to create a brand new row in the database.
    <br> D. It deletes the magazine.
13. If you call magazineRepository.save(mag) and the mag.getId() is 3, what does Spring Data JPA do?
    <br> A. It creates a second copy of magazine 3.
    <br> B. It throws an Ambiguous ID exception.
    <br> C. It performs an SQL UPDATE to modify the existing row with ID 3.
    <br> D. It ignores the save command.
14. What does th:replace="~{fragments/navbar :: header}" accomplish?
    <br> A. It deletes the navbar.
    <br> B. It replaces the current HTML tag with the contents of the specified fragment, allowing for reusable layouts.
    <br> C. It redirects the user to the navbar page.
    <br> D. It changes the color of the header.
15. What is the central "Front Controller" component that intercepts all web requests in Spring MVC?
    <br> A. The DispatcherServlet
    <br> B. The ApplicationContext
    <br> C. The JpaRepository
    <br> D. The CommandLineRunner
16. Which of the following is an example of a "Natural Template"?
    <br> A. A Java class that writes HTML using System.out.println.
    <br> B. An XML file used for configuration.
    <br> C. A Thymeleaf .html file that can be opened and viewed in a browser even without the server running.
    <br> D. A SQL script.
17. What is the default port that the embedded Tomcat web server uses in Spring Boot?
    <br> A. 3306
    <br> B. 80
    <br> C. 8080
    <br> D. 443
18. In Thymeleaf, what syntax is used to create dynamic, context-aware URL links?
    <br> A. ${/path}
    <br> B. @{/path}
    <br> C. #{/path}
    <br> D. *{/path}
19. Why do we avoid putting an infinite while(true) menu loop inside a Web Application's CommandLineRunner?
    <br> A. It consumes too much database memory.
    <br> B. It blocks the main thread, preventing the Tomcat Web Server from starting up and serving pages.
    <br> C. It causes Thymeleaf to crash.
    <br> D. It deletes the database tables.
20. What is the primary purpose of the Post/Redirect/Get (PRG) pattern?
    <br> A. To make web pages load faster.
    <br> B. To secure passwords.
    <br> C. To prevent duplicate form submissions if a user clicks the browser's "Refresh" or "Back" buttons.
    <br> D. To allow users to upload files.