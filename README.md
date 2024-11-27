java c
ITS66704 (Sept 2024)
Advanced Programming
Assignment Task 2  Task 3 (Group Project)
15% (PART A - ANALYSIS AND DESIGN)
15% (PART B - DEVELOPMENT)
OBJECTIVES (MLO3)
The objectives of this assignment are to enable you to:
1. MLO3 Construct the program solutions using object-oriented programming language and approach.
Scenario
Fitness Tracker Application (FTA) Design and Development
In this group project, students will have the opportunity to challenge their knowledge and skills by developing an innovative and usable Fitness Tracker Application (FTA). The development of a Fitness Tracker Application involves creating an intuitive interface that allows users to set and track fitness goals, log activities, and monitor progress over time.
Background:
The project will be divided among the team members. One group will be responsible for building the user profile management and fitness goal-setting features. Another group will handle the exercise logging module, allowing users to input details like duration, type of exercise, and calories burned. A third group will focus on data visualization, creating charts and graphs that display progress in key areas like weight, distance run, or calories burned over time. Additional features, such as a nutrition and diet planning module, could be developed by another team, allowing users to log their meals and track nutritional intake. Advanced functionality could include integrating data from wearable devices (optional) and providing real-time updates on user activity. Throughout the project, collaboration will be required to ensure smooth data flow between the different modules, ensuring an efficient and user-friendly fitness tracking experience.
Objectives:
1. To develop a comprehensive understanding of the application development process, from conception to completion.
2. To demonstrate creativity, problem-solving skills, and attention to detail in designing and implementing a most viable prototype (MVP).
3. UI/UX Design and Implementation:
a. Understand and apply principles of user-centered design to create an intuitive, aesthetically pleasing interface that enhances user experience.
b. Develop interactive and responsive layouts using JavaFX or Swing, focusing on form. inputs, data visualization, and user feedback mechanisms.
4. Event Handling and Data Binding using different UI components:
a. Learn how to handle various user interactions such as form. submissions, button clicks, and real-time updates.
b. Implement data binding to seamlessly connect the user interface with underlying data models for smooth updates and real-time data display.
5. Data Management and Persistence:
a. Design and implement data structures for managing user profiles, exercise logs, and fitness goals.
b. Learn techniques for persisting data, such as using local storage, file systems, or integrating with databases to save and retrieve user information
6. Modular Programming and Team Collaboration:
a. Gain experience in modular software development by dividing tasks into separate modules (e.g., user profiles, logging activities, data visualization) and integrating them cohesively.
b. Practice collaboration using version control systems (e.g., Git) to manage contributions from multiple team members, ensuring smooth project development.
7. Data Visualization:
a. Learn how to generate charts and graphs to represent user progress, exploring libraries for data visualization and how to dynamically update visuals based on user input.
b. Develop skills in managing real-time data updates for tracking fitness metrics such as calories burned, distance run, and weight loss.
8. Integration with External Devices (Optional):
a. Explore how to integrate third-party APIs or wearable devices (e.g., fitness trackers) to import real-time data into the application, enhancing the application’s functionality and realism.
9. User Authentication and Security:
a. Implement secure login and user authentication, applying security measures such as password hashing and role-based access controls to ensure data privacy and protection.
You are required to assemble a team of Java developers (2 – 6 members) to design and implement the Fitness Tracker Application. In this assignment, your team must use an object-oriented approach to model the main application classes, their subclasses (if any) and their corresponding attributes and methods. The application must have a relevant layout, data and corresponding business logic.
Each member must contribute to the design of at least one class and/or subclass definition. In addition, group members may collaborate with people from other faculties or industries who have the domain knowledge to define the scope and coverage of your intended FTA.
You may want to refer to the article here (Part 1-5) to kick-start your project.
• Note that database usage is not allowed for this assignment. You must use Text or Binary File I/O for persistent data storage on a local machine. The Data Access Object (DAO) hence must be redesigned to cater for local file access.
• You do not need to develop the web service endpoints. Instead, you should just develop the common classes and methods in your application as a substitute for the endpoints. The API request will be submitted by method calls.
• For the graphics, you may implement each of the above using suitable UI components available in Java FX or Swing. Remember to document and justify your UI selection.
Figure 1 below provides an overview of basic fitness app functionality.
Figure 1: Basic Fitness App Functionality
The intended system should maximize the implementation of object-oriented concepts such as instantiation, encapsulation, inheritance, and polymorphism. The data storage method is confined to what is covered in the syllabus, i.e., text and binary files only and does not cover various SQL, network, or cloud storage. You must strictly adhere to this rule. No marks will be awarded to data storage methods that are not within the syllabus coverage.
Step 1: Conceptualization
The step involves brainstorming and defining the core objectives and features of the fitness tracker. The goal is to establish the vision for the app.
Identify Core Features: Begin by defining the key functionality the app will provide. For a fitness tracker, this might include:
• User Profiles for tracking personal data (e.g., name, weight, fitness goals).
• Fitness Goals to allow users to set targets (e.g., weight loss, distance, calorie goals).
• Exercise Logging for users to record their daily workouts (e.g., type, duration, intensity).
• Nutrition and Diet Tracking for users to monitor their meals, calories, and nutrients.
• Progress Visualization through charts and graphs showing fitness trends over time.
• Wearable Device Integration (optional) to automatically sync data from fitness devices.
• User Authentication for security and data protection.
Target Audience: Define who the users are (e.g., fitness enthusiasts, people aiming to improve their health). This helps tailor the features to user needs.
Technology Stack: Decide the technology to be used, such as:
• JavaFX or Swing for the user interface.
• Local DAO for storing data.5
• APIs for integration with fitness devices (optional).
Team Roles: Assign roles to each team member, e.g.:
• UI/UX designer
• data management
• Class and Module developer
• visualization specialist
• Security expert for authentication and data protection
Step 2: Prototyping
Prototyping involves creating a mock version of the application, usually focusing on the user interface and flow without fully functional code.
Wireframes: Start with low-fidelity wireframes that outline the layout and flow of the app. This can be done on paper or using digital tools like Figma or Adobe XD.
• Include screens for user profiles, logging workouts, diet tracking, and progress graphs.
• Sketch how users will navigate between screens (e.g., menus, buttons代 写ITS66704 Advanced Programming Assignment Task 2 & Task 3Java
代做程序编程语言, icons).
Basic UI Flow: Develop a clickable prototype that shows the user’s journey through the app:
• Login/Sign-Up page
• Dashboard showing progress and goals
• Screens for logging workouts and meals
• Data visualization page for graphs
Feedback Gathering: Test the prototype with potential users to gather feedback. Ensure that the navigation is intuitive, the layout is user-friendly, and the key features are easy to access.
Step 3: Art and Design
In this step, focus on creating a high-fidelity design of the app, working on both the aesthetics and the technical architecture.
UI/UX Design:
• Visual Design: Choose color schemes, fonts, button styles, and icons that align with the brand identity of the app. Ensure that the interface is clean and visually appealing.
• User Interaction: Map out how users will interact with different elements on the screen (e.g., input forms, buttons, sliders). Ensure the app is responsive and accessible on different devices.
• Responsive Layouts: Consider how the app will adapt to various screen sizes (e.g., desktop, tablets).
Data Access Objects (DAO):
• Entity-Relationship (ER) Diagrams: Design the DAO to store user data (e.g., fitness goals, exercise logs, meal entries). The data store might include:
• User: Stores personal details, login credentials.
• Workouts: Stores logs of each workout.
• Nutrition: Tracks meals and calorie intake.
• Progress: Logs metrics like weight, distance run, calories burned.
• Decide on suitable file types and structure to store the data.
System Architecture:
• Decide on the communication between the UI and the data management.
• Plan how data will be fetched from the DAO and displayed in the UI.
• Consider integrating APIs for device syncing.
Step 4: Implementation
This is the most extensive step, where the actual coding and development of the app happens. This stage will be broken into sub-tasks that correspond to the previously designed modules.
User Authentication:
• Implement login and registration forms using JavaFX/Swing.
• Add password encryption for security.
• Implement a session system to keep users logged in.
User Profiles and Fitness Goals:
Develop forms for users to input their personal data and set goals (e.g., weight loss, distance targets). Store the data in the database and display it on the dashboard.
Exercise Logging Module:
• Create a UI for users to log their workouts (e.g., exercise type, duration, calories burned).
• Include options for adding custom workouts.
• Save workout logs to the database and retrieve them when needed.
Nutrition and Diet Tracking:
• Build a form. to allow users to input their meals (e.g., food items, calories, macronutrients).
• Use a database of common food items or integrate a third-party API to retrieve nutrition data.
• Display nutritional summaries and allow users to track their daily intake.
Data Visualization:
• Implement charts using libraries like JFreeChart to show users' progress over time.
• Visualize key metrics like weight, calories burned, and distance covered.
• Allow users to filter data by date range and specific metrics.
Wearable Device Integration (Optional):
• Integrate APIs to sync data from fitness devices like smartwatches.
• Automatically log workouts and display them in the app.
Data Persistence and Storage:
• Ensure all user data (workouts, meals, progress) is properly stored in the data files and can be retrieved efficiently.
• Implement backup mechanisms for data safety.
Step 5: Optimization
After the core functionality is implemented, optimize the app for performance, usability, and scalability.
Code Optimization:
• Refactor the codebase to improve efficiency and readability.
• Optimize database queries to reduce load times for retrieving user data.
Performance Tuning:
• Test the app for performance under different conditions (e.g., high number of users, large datasets).
• Address any slow-loading elements, especially in the data visualization module.
User Experience (UX) Refinement:
• Use feedback from initial testing to make the app more user-friendly. For example, reduce the number of steps needed to log a workout or set a fitness goal.
• Ensure the UI is responsive, and that the app runs smoothly on different screen sizes.
Security Enhancements:
• Strengthen the authentication system, adding features like two-factor authentication.
• Ensure that sensitive user data (passwords, personal info) is encrypted and stored securely.
Step 6: Presentation
In the final step, the team presents the completed application to stakeholders or peers, showcasing the app’s functionality, design, and impact.
Presentation Materials:
• Create a slide deck that summarizes the project's goals, development process, and key features.
• Include demo videos or live demonstrations showing how users can log in, track their workouts, monitor nutrition, and visualize progress.
Highlight Key Features:
• Emphasize unique or standout features such as wearable device integration, real-time data visualization, or the app's seamless user experience.
Technical Walkthrough:
• Explain the system architecture and how the different modules (UI, database, security) work together.
• Share code snippets or flowcharts to illustrate key technical decisions.
Challenges and Solutions:
• Discuss the challenges faced during development (e.g., performance issues, security considerations) and how they were resolved.
Future Enhancements:
• Suggest potential future improvements, such as more advanced data analytics, gamification (e.g., fitness challenges), or support for additional wearable devices.
BONUS (Extra credit)
1. Your application has full support for the basic operations of persistent storage for saving user data.
2. The use of encryption to secure the user’s password is highly desirable.
3. Data is stored in a binary data file.
Follow proper coding style, naming convention, indentation, and comment on the code appropriately. Assessment marks will also take aesthetics (how beautiful the system and user interface are) and uniqueness (how your application differs from that of other groups) into consideration.
Part A – Analysis and Design (30%)
Conduct an in-depth analysis and design of the solution to the problem above. Specifically, you need to provide the following:
1. Works responsibilities and delegation.
2. Documentation of the system including the concepts, design, and prototype.
3. Your UML use case and UML class diagrams.
4. Your user interface (static) prototypes.
Deliverables
A well-structured and properly formatted academic document that contains the detailed specifications for the proposed system, associated solution high-level design diagrams, and interface prototype diagrams. Ensure that your submission includes a cover page which shows your group member names and student IDs. All submissions should be in pdf format (ProjectPartA_GroupNo.pdf).
Part 1 Due Date: 22/11/2024 11:59pm submit via mytimes.taylors.edu.my submission link.
Part B - Development (30%)
Develop the system based on your analysis and design in Part A. Specifically, you need to provide the following:
1. Java source code of the application (system) including the resource files (pictures etc.).
2. Relevant screenshots to prove adequate testing are done.
3. Your OOP documentation to point out where the OOP concepts are implemented in your application.
Deliverables
Your pdf report along with your zipped application project folder. Ensure that your submission includes a cover page which shows your group member names and student IDs. File names should be named as follows:
“ProjectPartBReport_GroupNo.pdf” – The pdf copy of your report
“ProjectPartBProgram_GroupNo.zip” – The application project folder
Part 2 Due Date: 13/12/2024 11:59pm submit via mytimes.taylors.edu.my submission link.



         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
