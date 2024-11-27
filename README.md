java c
ITS66704   (Sept 2024)
Advanced   Programming
Part A – Analysis and Design
2. Concepts
Our guiding principles include ongoing motivation, scientific advice,   and the user's health experience. Everybody has a distinct body, lifestyle, and set   of   goals,   and   our production   team is in agreement that fitness is a personal   journey.   Personalization   "for   each person"   must be the main emphasis of   our software design. Our   goal   is to provide   customers   with   a   personalized and distinctive sports   experience.
Core features
The software is divided into three modules: User Management, Fitness   Program   and   Tracking, Data Analysis and Feedback.
The user management module includes   Sign Up (new users enter their name and password to   complete the registration), Log In (registered users enter their name and password to verify the   identity   of   the   login), User   Profile   (management   of   the   user's   basic   information   such   as name, weight,dateofbirth, gender, body   fat   percentage, etc.).
Fitness program and tracking module contains   the following functions: Workout   Tracking   (responsible for recording the user's workout data. It is responsible for recording the user's   workout data, such as title, date, duration, workout   area,   and   calculating   the   total   calorie   consumption), Workout Plan (which can assist the user in determining   their   weekly   exercise      goals and body weight target), Diet Tracking (which keeps track of   the user's   daily   calorie               intake as well as the meals and drinks they   consume),   and   Online   Coach   (which provides the   links to a variety of   exercise instructional videos: HIIT, Yoga,   Stretching, Cardio,   etc.).
The Data Analysis and Feedback module includes Fitness Trends (which   generates   different      images, such as a bar graph that shows more   clearly   the number   of   hours   the   user has   trained   in the month, a pie chart that shows the distribution   of   body parts the user has worked   out   in      the   month, as   well   as   a   graph   that   shows   changes   in   users'body   weight   and   a   bar   chart   that          shows the trend in calorie consumption). It also has   Customer   Support, which makes   it   easy      for users to give feedback and contact the   developers.
Targeted audience
The software covers running, yoga, meditation, cycling and   other   sports,   as well   as   user-recorded sports progress, diet and other aspects, generating   exclusive user's   own body   and health trends. Daily fitness training courses are diversified,   and users   can   divide them         according to usage scenarios, intensity, training needs, equipment, etc., which   can basically   cover all the needs of   daily training. Quantitative recording and analysis   of   sports   data   and    visualization   of   effects   can   help   improve   users'enthusiasm   for   exercise.
The software provides online coaches, customized intelligent training plans   according to   personal   needs,and   voice   guidance   training   throughout   the   process, which   is   very   friendly   to   novice fitness enthusiasts. The software is   suitable   for people who value   appearance,   love   health, pursue quality of   life, have the need to lose weight, want to record life,   and pursue self-discipline.
Technology
Tools and technologies used:
1. IntelliJ IDEA: Chosen for its robust Java   development   environment   and   excellent      JavaFX support. Its code completion and debugging   tools   significantly   improved   our   development efficiency.
2. JavaFX:   Selected as the primary framework due to its powerful UI   capabilities   and   cross-platform. compatibility. It allowed us to create a visually   appealing   game with smooth animations.
3.   Scene Builder: Utilized to design the game's UI layouts visually. This tool   accelerated   our UI development process and ensured consistency across different   screens.
4. JDK 21: The latest stable version at the time   of   development,   offering   performance   improvements and new   language features that enhanced our   code   quality   and   efficiency.
5. Libraries:It is an external plug-in that can realize the   function   of   making   charts.   It processes, maps, and renders user data, and finally outputs   it   into   a visual   chart to provide users with changes in body movement in recent months or weeks, as well   as the   trend   of changes in exercise volume. It allows users to compare   and   analyze their real-time physical   status, which   helps   to   improve   users'enthusiasm   for   exercise.
6. Multithreading: Multithreading is a programming technique that allows a program to   run   multiple threads at the same time. Threads are the   smallest units   that   the   operating   system   can   independently schedule and execute. They share the   memory   space   and   resources   of   the   same   process, but can execute code independently. The most important thing   is   that   when   one   of the threads is damaged, the others can   still run   normally.
7. API: (Application Programming Interface)It is an interface between   one   system   and another, defining a set of   rules and protocols to   allow   communication   and   interaction between   different software or services. It can   generate   a   link   for users to   copy   and paste   and   send to other friends.
3. Design
3.1 OO   concepts
Abstraction: In Java, abstraction simplifies system complexity   by   hiding   complex   implementation details and showing only the functions required by   users   (Rahul   bangari,   2024a).
The developer can define   a User abstract class   in   the   software.   The   User   abstract   class   contains two basic attributes: name and password, which represent the basic identity of   the user.
There are two behavior. methods: login()   : provides the login function to verify whether the   name and password entered by the user match. updateProfile()   : Allows   users to modify their   personal information (such as updating user names or passwords). To increase   the   flexibility      of   the system and ensure that the interface logic   is   separated   from the   data processing.   The developer chooses to implement the abstraction with an interface, hiding the   methods   and   basic properties in the abstraction and displaying only the necessary   functionality:   signUp(),   login(),updateProfile().
   
Interface:In the Java programming language, an interface is an   abstract type   that   is used   to define a class's behavior. Java interfaces provide abstract methods and   static   variables(Kumar   and   Nitsdheerendra, 2016).The developer declares three methods by defining a UserActions interface:   signUp(),   logIn(),   and updateProfile(). These methods are marked as abstract methods, meaning that   any   class that inherits the interface needs to implement them, otherwise an   error will be   thrown.
The developer can then create an Abstract Class User   and have   it   implement   the UserActions   interface. In the User class, the implementation method is provided: signUp()   :   responsible   for user registration, set the name and password of   the user. logIn()   : Responsible   for user login. Check whether the name and password entered by the user are correct.   If   correct, the login succeeds. updateProfile()   : Allows users to update personal information, such as changing their name or   password.
All classes that implement the UserActions interface have the same basic behavior   and methods, ensuring code consistency and maintainability. And if   you need to   add new user types or new features in the future, you don't need to modify   the   existing   code,   you   just   need   to extend the interface or implementation   class
Encapsulation: Encapsulation   in   java   is   to   provide   data   protection   to   avoid   the   disclosure   of sensitive user information.(geeksforgeeks, 2017).
To protect the user's personal information and data records, sensitive information   (such   as   the   user's password) and data records (such as daily   calorie intake   and   water   intake)   can   be   made   private fields in an encapsulation manner that allows   secure   access   or modification   only through public methods such as setPassword() and getPassword().   This   design   effectively avoids direct manipulation of   data, reduces the risk of   data leakage or tampering,   and   ensures consistent access control.
Inheritance:An essential component of   Java OOPs is inheritance, the   function   is   avoid   duplicate code and achieve extensible interface functionality.(Rahul bangari,   2024).
Inheritance applications in this software can be reflected   in:The developer can define a base class called   'User'   that   represents   properties   and   functionality common   to   all   users. Each   'User' object   contains' name   '(username)   and'passwo代 写ITS66704 Advanced Programming Part A – Analysis and DesignJava
代做程序编程语言rd   '(password) properties, in   addition   to   two   methods:'signUp() 'for   registering   the   user, and'    logIn() 'for logging in. These methods are fundamental   features   that   are   shared by   all   users.
Then define the RegularUser class, which inherits from the User   class.   The RegularUser   class   is a subclass tailored to ordinary users, such   as   fitness   enthusiasts. Not   only   does   it   inherit   all      the attributes and methods of   the User class, but it also   adds   some   functionality   specific   to   ordinary users. For example, the RegularUser class adds attributes   such   as   diet_tracking   (diet   plan) and Workout_Plan (exercise plan), workout_Tracking (exercise tracking), etc.   These attributes enable Regularusers to better track and customize an individual's   fitness progress and diet plan.
In addition, the RegularUser class provides additional methods, dietData_()   for recording diet   information and exerciseData() for recording exercise information. These   features   are required by ordinary users when using the system.
Through this inheritance structure, the code realizes the function reuse   and   extension.   As   a   superclass,the   User   class   provides   basic   user   management   functionality, while   the   RegularUser   class   further   enhances   the   functionality   of   specific   users. If   we   need   to   provide coach   users   ('coachusers') with   the   ability   to   manage   other   users   in   the   future, we   can   continue to inherit the User class and add specific   functions   to   CoachUser,   so   as   to   achieve   the   extensibility   of   the   code.
This design allows users in different roles to share   common   functions, while   also providing   specific customization functions for different roles.
   
Composition is an object-oriented design principle that refers to building more complex   objects by combining objects together instead of   using inheritance. It   is necessary   to   create   a basic interface that can be implemented by different training actions,   such   as PushUp,   Plank, Squat. In Composition, the relationship between different classes is inseparable,   and   you   have   me and I have you. (Rahulbangari,   2024a)
It can divide the software into different   categories   (such   as Workout   PLans,   Workout   Tracking, etc.). Provide different and personalized training plans, each of   which may   contain   multiple   training   modes   (such   as   aerobic   exercise, strength   training,   etc.),which   are   combined to create a complete training plan.
Benefit: Composition can improve code reusability and maintainability, meet the   diverse needs in fitness scenarios, and facilitate the rapid update   of   system   functions   according   to   business needs. It can not only better support user needs, but also maintain high   development   efficiency and quality.
Aggregation is a design pattern that represents the loose relationship between the whole   and   the   part. It   is   used   to   represent   the   "whole-part" relationship, and   the   lifecycle   between   the whole and the part is independent. Aggregation is different from   Composition.   Although   the   classes in Aggregation are related, they can exist separately   even   if   they   are   separated.
However, they are also very important to each other.   (Rahulbangari,   2024a)A training plan can include multiple fitness movements, and users can   manage   their   own   fitness   data   records. Multiple   coaches   can   teach   the   same   course,   and   the   lifecycle   of   the course and the coach is independent, allowing   for arbitrary   combinations.
Aggregation can improve the modularity, reusability and flexibility of   the   software.   Because   it can be used as an independent module, it   is   easy to   count   and   display,   and the   user   data   is      separated from the achievement module, making the system more   flexible,   so it   can   more efficiently manage the relationship between objects, reduce coupling, and improve the   flexibility   and   maintainability   of   the   system.
Association represents an interactive or cooperative relationship between two or more objects, without   lifecycle   dependency   and   ownership   relationship. Association, Composition,   and Aggregation are completely different concepts. In Association,   although the   classes   of   the relationship exist with each other, they are completely   independent,   and   one   class   is   dispensable to other classes.(Rahulbangari, 2024a)
For example, the many-to-many association relationship between courses and users, coaches      and users, and users and exercise records. This relationship is not   strongly   dependent, usually   manifested   as   "related   but   not   part   of   the   whole", which   is   different   from   the   nature   of Aggregation.
Association can provide flexible interaction between objects, enhancing the   scalability, maintainability and understandability of   the system. Choosing different   design methods   can   more clearly express the relationship between classes and enhance   the   flexibility   and maintainability   of   the   code.
3.2 Patterns
Introduction to PatternsDesign patterns are reusable solutions to common software   design problems. By   applying   design patterns, the system can achieve modularity, maintainability, and   scalability.   In this   section, the patterns used in our application are explained   in   detail.
1. Model-View-Controller (MVC)
Purpose:The MVC pattern is implemented to separate concerns in   the   application,   ensuring   a   clear   distinction between the presentation layer, the business logic, and user interactions.(New      York (2011))
Application in the   System:
Model: Encapsulates the application's data and business logic. For instance,   the   Diet   Model   handles the user's diet tracking data, such as meals,   calories,   and total water   intake.
View: Represents the user interface, displaying the input   forms and   results   for modules   like   Diet Tracking and Workout Tracking.
Controller: Manages user interactions (e.g., submitting diet data)   and updates both   the   Model and View accordingly.
Justification:Keeps the user interface separate from the business logic, allowing   independent modifications.
Promotes testability as Model and Controller can   be tested independently   from   the   View.
2. Data Access Object   (DAO)
Purpose:
DAO is used to abstract and encapsulate all   database   interactions,   such   as   saving user   diet   and workout data. This isolates persistence logic from business logic.(2021.UKEssays.   )
Application in the   System:
DAO is used to manage user   records in modules like Diet Tracking   and Workout   Tracking.
For example, a Diet DAO class handles database   operations   for   storing   and retrieving   diet   data.( Feyza Nur. 2018)
Justification:
Separates the persistence logic from the application's business logic, ensuring   cleaner   code.   Makes   it   easier   to   switch   database   implementations   if   needed.
3. Data Transfer Object   (DTO)
Purpose:
DTO is used to transfer data between the different layers of   the   application   in   a   structured   manner.((WODA 07). IEEE, 2007:   5-5.)
Application in the   System:
DTOs are used in the application to pass data between Controllers   and   Views,   such   as   transferring user diet details or work out   details.
Example classes: Diet DTO, Workout DTO.   Justification:
Reduces   the   complexity   of   data   transfer   between   layers.
Improves code readability by grouping related attributes   into one   object.
4.   Singleton
Purpose:
The   Singleton pattern ensures that a particular class has only one   instance   and provides   a   global point of   access to it. This is commonly used for managing   shared   resources   like   database connections.(John Wiley    Sons, 2013.)   Application in the   System:
The Database Manager class is implemented as a   Singleton   to manage   database   connections   across the entire application.
Justification:
Prevents the creation of   multiple database connections, ensuring   efficient resource usage. Provides a centralized control point for database   operations.
5. Dependency Injection
Purpose: Dependency Injection is used to decouple object creation   and usage.   It   allows   objects to be injected into a class instead of   being   created within   the   class.
Application in the   System:
Controllers like Diet Controller and Workout Controller receive dependencies   such   as   Diet   Service and Workout   Service through dependency injection.(training[J]. 2022.)
Justification:
Enhances   modularity   by   allowing   the   injection   of   mock   objects   for   testing   purposes.   Simplifies maintenance by decoupling classes and their dependencies.

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
