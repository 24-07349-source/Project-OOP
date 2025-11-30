 FloodGuard: Ethical Flood Control and Monitoring System
 
 Team GelLyRob – IT-211O
 
 Gonda, Chris Angel H.

 Mahiya, Lyta Mae M.
 
 Rivera, Rob Gunther G.


📌 Project Overview

FloodGuard is a console-based Java application designed to simulate an ethical flood monitoring and response system. It models real-world environmental monitoring practices and integrates ethical software principles such as transparency, honest reporting, and user-centered communication.

The project is inspired by modern research on flood detection technologies.
Pahuriray & Cerna (2025) emphasize the importance of IoT sensors, real-time data collection, and machine learning for disaster preparedness, while Sengupta (2024) highlights scalable IoT frameworks and neural networks for improved flood detection. These studies guided the design of FloodGuard’s simulated monitoring system.

The application allows users to manage regions, update water levels, and assess flood risks using object-oriented programming concepts.


🧠 OOP Concepts Used

Encapsulation

Private fields in the Region class (name, waterLevel, safetyThreshold).

Dedicated getters and setters control access.

Input validation prevents negative or invalid data.

Inheritance

UrbanRegion and RuralRegion both extend the abstract Region class.

Each region type uses different sensitivity levels for flood evaluation.

Polymorphism

evaluateFloodRisk() is overridden in each subclass.

Urban areas use stricter thresholds; rural areas allow more water level variance.

Abstraction

Region defines shared properties and methods.

Subclasses implement specific risk evaluation logic.

Exception Handling

try-catch blocks handle invalid numeric input.

Protects against runtime errors and ensures stable program execution.


📁 Program Structure

Main Classes

Region (abstract)

Base class containing attributes for name, water level, and safety threshold.

UrbanRegion (subclass)

Uses stricter thresholds due to infrastructure sensitivity.

RuralRegion (subclass)

More flexible water-level tolerance.


📊 Text-Based Class Diagram (Simplified)

                   +----------------------+
                   |      Region (abs)    |
                   +----------------------+
                   | - name               |
                   | - waterLevel         |
                   | - safetyThreshold    |
                   +----------------------+
                   | + evaluateFloodRisk()|
                   | + generateAlert()    |
                   +-----------+----------+
                               |
                -------------------------------
                |                             |
     +---------------------+       +---------------------+
     |    UrbanRegion      |       |    RuralRegion      |
     +---------------------+       +---------------------+
     | threshold = 10.0    |       | threshold = 12.0    |
     | overrides evaluate  |       | overrides evaluate  |
     +---------------------+       +---------------------+

                     +----------------------------+
                     |     FloodGuardConsole     |
                     +----------------------------+
                     | main program logic         |
                     | manages regions (List)     |
                     +----------------------------+


How to Run the Program

1. Save the Java File

Make sure the filename matches the public main class.

2. Open Command Prompt / PowerShell

Navigate to the folder containing your .java file:

cd path\to\your\project

3. Compile
javac FloodGuardConsole.java

4. Run
java FloodGuardConsole

5. Interact with the Menu

The main menu will appear, allowing you to:

Add regions

Update water levels

View risk assessments

List all regions


🖥️ Sample Output

<img width="753" height="387" alt="Screenshot 2025-11-30 113648" src="https://github.com/user-attachments/assets/1e260853-9e10-40ad-a466-3223a89cf5df" />








✍️ Authors & Acknowledgements

This project was created by Team GelLyRob:

Chris Angel H. Gonda – Leader, writer, researcher, documentation

Lyta Mae M. Mahiya – Writer, researcher, documentation

Rob Gunther Rivera – Console programming, system development

The division of tasks allowed each member to contribute based on their strengths, ensuring efficient workflow and creativity in both writing and system implementation.

Special thanks to:

Ms. Christiana Grace Alib — for providing continuous guidance, feedback, and encouragement.

Families, loved ones, and friends — for their unwavering support.

Each team member — for their dedication, effort, and collaboration that led to the project's success.


🚀 Future Enhancements

The team recommends the following improvements:

1. Modernized Interface

Add colorized terminal UI or migrate to GUI frameworks (JavaFX, Swing).

2. Expanded System Capabilities
   
Asynchronous background processing.

Region filtering and sorting options.

More advanced modeling of flood progression.

3. Database Integration
   
Store region data permanently using MySQL or SQLite.

Enable long-term flood history tracking.


📚 References

Pahuriray, A. V., & Cerna, P. D. (2025). IoT-enabled flood monitoring and early warning systems. International Journal of Computer Science and Mobile Computing.
(https://www.ijcsmc.com/docs/papers/April2025/V14I4202515.pdf
)

Sengupta, S. (2024). IoT-based flood detection and management systems in smart cities. RAMD: Recent Advances in Management and Development.
(https://ramd.reapress.com/journal/article/view/53
)

Yi, X., Chen, H., & Wang, Z. (2024). Cutting-edge sensor technologies for improved flood management. Sensors.
(https://pmc.ncbi.nlm.nih.gov/articles/PMC11548130/
)


FloodGuardConsole (main class)
Handles menu navigation, input, region management, and overall workflow.# Project-OOP
