



1. Introduction
This report presents the design and implementation of a Crop Disease Prediction Expert System developed to assist farmers in diagnosing diseases affecting maize and tomato crops.
The system uses a knowledge-based approach to identify diseases based on observable symptoms and provides recommendations for treatment. It combines knowledge representation techniques with practical implementation using Prolog and Python.

2. Crops Covered
The expert system focuses on the following crops:
•	Maize
•	Tomato
These crops were selected due to their economic importance and the availability of well-documented disease information.

3. Identified Crop Diseases
A wide range of diseases affecting maize and tomato were identified and included in the system. Each disease is associated with specific symptoms, descriptions, and treatment recommendations.

4. Disease Symptoms Knowledge Base
Each disease in the system is linked to a set of observable symptoms. These symptoms are used to guide the diagnostic process.
The knowledge base also includes:
•	Disease descriptions
•	Recommended treatments

5. Knowledge Representation
The system uses a knowledge-based representation implemented in Prolog.
Each disease is stored using the structure:
disease_info(Crop, Disease, Symptoms, Description, Recommendation)
This allows the system to store both diagnostic and advisory information in a structured format.

6. System Implementation
The system was implemented using:
•	Prolog → for the knowledge base
•	Python (Tkinter) → for the graphical user interface
Prolog stores all disease-related knowledge, while Python handles user interaction and communicates with the Prolog system to retrieve relevant information.

7. System Architecture
The system consists of three main components:
i. User Interface (Python - Tkinter)
•	Allows users to interact with the system
•	Displays symptoms and results
ii. Knowledge Base (Prolog)
•	Stores diseases, symptoms, descriptions, and recommendations
iii. Interaction Layer
•	Python queries Prolog to retrieve disease data
System Flow:
User  Python Interface  Prolog Knowledge Base  Python User


8. Project Structure
The project is organized into the following modules:
•	docs/
o	Contains documentation such as the knowledge report
•	interface/
o	Contains the Python application (app.py)
o	Handles user interaction and display
•	knowledge_base/
o	Contains the Prolog file (expert_system.pl)
o	Stores all expert knowledge
•	README.md
o	Provides project overview and usage instructions

9. Code Implementation
Prolog Knowledge Base Example
disease_info(maize, 'Maize Rust',
    ['Reddish-brown spots on leaves', 'Yellow patches on leaves', 'Leaves drying early'],
    'A fungal disease causing reddish-brown pustules on leaves.',
    'Apply fungicides such as mancozeb.').
Query Predicate Example
get_all_diseases(Crop, Diseases) :-
    findall(D, disease_info(Crop, D, _, _, _), Diseases).
Python Integration Example
self.kb = KnowledgeBase()
Python uses this connection to retrieve disease information from Prolog.

10. System Interaction
The system operates as follows:
1.	The user selects a crop (maize or tomato)
2.	The system retrieves all diseases associated with the crop
3.	Symptoms for each disease are displayed
4.	The user confirms whether the symptoms match (YES/NO)
5.	The system records confirmed diseases
6.	Final results are displayed with:
o	Disease name
o	Symptoms
o	Description
o	Recommendation

11. Testing and Results
The system was tested using different symptom combinations.
Test Case 1
•	Crop: Maize
•	Symptoms:
o	Reddish-brown spots
o	Yellow patches
o	Early leaf drying
Result:
•	Disease Identified: Maize Rust
•	Recommendation: Apply fungicide and use resistant varieties


Test Case 2
•	Crop: Tomato
•	Symptoms:
o	Brown spots with rings
o	Yellow lower leaves
o	Leaf drop
Result:
•	Disease Identified: Early Blight

Test Case 3
•	No matching symptoms
Result:
•	System indicates no disease detected

12. Challenges Faced
The following challenges were encountered:
•	Similarity of Symptoms
Some diseases share similar symptoms, making diagnosis difficult
•	Integration Complexity
Connecting Python with Prolog required careful handling
•	User Input Accuracy
Users may not correctly identify symptoms

13. Final Conclusion
The Crop Disease Prediction Expert System successfully demonstrates the application of artificial intelligence techniques in agriculture.
By combining a Prolog-based knowledge system with a Python user interface, the system is able to:
•	Diagnose crop diseases
•	Provide useful recommendations
•	Assist farmers in decision-making
This project highlights the effectiveness of knowledge-based systems in solving real-world problems.















