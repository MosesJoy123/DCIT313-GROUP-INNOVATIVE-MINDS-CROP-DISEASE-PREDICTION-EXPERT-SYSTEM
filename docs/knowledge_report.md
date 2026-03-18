1. INTRODUCTION
Agriculture is a key sector in food production, and crop diseases significantly reduce both yield and quality. Farmers often find it difficult to diagnose diseases accurately due to similar symptoms across different conditions. To solve this problem, an expert system can assist by providing accurate diagnosis and recommendations.
This report presents the development of the knowledge base for a Crop Disease Expert System. The knowledge base is responsible for storing structured information about diseases and enabling intelligent decision-making.

2. OBJECTIVE OF THE KNOWLEDGE BASE
•	Store crop disease knowledge in a structured format
•	Enable accurate diagnosis based on symptoms
•	Provide clear disease descriptions
•	Recommend effective treatments

3. KNOWLEDGE REPRESENTATION
The system uses Prolog for knowledge representation.
Each disease is represented as:
disease_info(Crop, Disease, Symptoms, Description, Recommendation)

4. DIAGNOSIS LOGIC
The system uses a rule-based approach:
•	Each disease is defined by three symptoms
•	Diagnosis occurs only when all symptoms match
•	This ensures high accuracy and reduces ambiguity

5. KNOWLEDGE BASE CONTENT
5.1 Maize Diseases
(15 diseases covered)
5.2 Tomato Diseases
(15 diseases covered)

6. KNOWLEDGE ACQUISITION
Knowledge was obtained from:
•	Agricultural guides
•	Crop disease manuals
•	Standard farming practices

7. QUERY MECHANISM
•	get_all_diseases(Crop, Diseases)
•	get_disease_info(Crop, Disease, Symptoms, Description, Recommendation)

8. CONCLUSION
The knowledge base provides a solid foundation for diagnosing crop diseases using structured rules. It is accurate, scalable, and practical for real-world use.

9. RULE BASE REPRESENTATION (IF–THEN RULES)
The system can also be expressed using IF–THEN rules for clarity.

**MAIZE DISEASE RULES**

IF Crop = Maize AND Reddish-brown spots on leaves AND Yellow patches on leaves AND Leaves drying early
THEN Disease = Maize Rust

IF Crop = Maize AND Yellow streaks on leaves AND Stunted plant growth AND Pale green leaves
THEN Disease = Maize Streak Virus

IF Crop = Maize AND Rectangular gray lesions on leaves AND Brown leaf edges AND Leaves drying prematurely
THEN Disease = Gray Leaf Spot

IF Crop = Maize AND Swollen galls on ears or leaves AND Black powder inside galls AND Distorted plant tissues
THEN Disease = Common Smut

IF Crop = Maize AND Yellow leaves AND White fungal growth under leaves AND Stunted plants
THEN Disease = Downy Mildew

IF Crop = Maize AND White mold on maize ears AND Pink fungal growth on ears AND Rotting kernels
THEN Disease = Fusarium Ear Rot

IF Crop = Maize AND White mold on ear AND Brown dry ears AND Kernels sticking together
THEN Disease = Diplodia Ear Rot

IF Crop = Maize AND Small brown spots on leaves AND Spots merging together AND Yellow leaves
THEN Disease = Anthracnose Leaf Blight

IF Crop = Maize AND Long cigar-shaped lesions AND Gray leaf patches AND Leaves turning brown
THEN Disease = Northern Corn Leaf Blight

IF Crop = Maize AND Small tan leaf spots AND Spots spreading on leaves AND Early leaf drying
THEN Disease = Southern Corn Leaf Blight

IF Crop = Maize AND Narrow yellow streaks on leaves AND Streaks turning brown AND Dry leaf tissue
THEN Disease = Bacterial Leaf Streak

IF Crop = Maize AND Mosaic light and dark green leaf pattern AND Narrow leaves AND Stunted plants
THEN Disease = Maize Dwarf Mosaic Virus

IF Crop = Maize AND Black powder inside the stem AND Weak and easily broken stalks AND Plant wilting
THEN Disease = Charcoal Rot

IF Crop = Maize AND Seedlings failing to emerge AND Brown stem lesions on seedlings AND Seedling collapse
THEN Disease = Seedling Blight

IF Crop = Maize AND Rotting roots AND Wilting plants AND Poor plant growth
THEN Disease = Root Rot

**TOMATO DISEASE RULES**
IF Crop = Tomato AND Brown leaf spots with concentric rings AND Yellow lower leaves AND Leaf drop
THEN Disease = Early Blight

IF Crop = Tomato AND Dark water-soaked spots on leaves AND White mold under leaves AND Rapid plant decay
THEN Disease = Late Blight

IF Crop = Tomato AND Leaves curling upward AND Yellow leaf edges AND Stunted growth
THEN Disease = Tomato Leaf Curl Virus

IF Crop = Tomato AND Sudden plant wilting AND Brown stem discoloration AND Plant death
THEN Disease = Bacterial Wilt

IF Crop = Tomato AND Yellow lower leaves AND Wilting in hot weather AND Brown streaks inside the stem
THEN Disease = Fusarium Wilt

IF Crop = Tomato AND Yellow V-shaped spots on leaves AND Lower leaves wilting AND Slow plant decline
THEN Disease = Verticillium Wilt

IF Crop = Tomato AND Small circular spots on leaves AND Dark borders around spots AND Yellow leaf areas
THEN Disease = Septoria Leaf Spot

IF Crop = Tomato AND Mosaic light and dark green leaf pattern AND Distorted leaves AND Reduced fruit yield
THEN Disease = Tomato Mosaic Virus

IF Crop = Tomato AND White powder on leaves AND Yellow leaves AND Leaf drop
THEN Disease = Powdery Mildew

IF Crop = Tomato AND Small dark spots on leaves AND Yellow halos around leaf spots AND Raised spots on fruit
THEN Disease = Bacterial Spot

IF Crop = Tomato AND Sunken lesions on fruit AND Fruit rotting during ripening AND Circular spots on fruit
THEN Disease = Anthracnose

IF Crop = Tomato AND Bronze or brown leaf color AND Ring spots on fruit AND Stunted plants
THEN Disease = Tomato Spotted Wilt Virus

IF Crop = Tomato AND Swollen knots on roots AND Yellow leaves AND Weak plant growth
THEN Disease = Root Knot Nematode

IF Crop = Tomato AND Dark spot at the bottom of fruit AND Rotting fruit tissue AND Premature fruit decay
THEN Disease = Blossom End Rot

IF Crop = Tomato AND Seedlings collapsing at soil level AND Soft stem base on seedlings AND Poor germination
THEN Disease = Damping Off

**FINAL NOTE**
The IF–THEN rules clearly show how the system makes decisions. When all conditions in a rule are satisfied, the system concludes the corresponding disease, ensuring accurate and reliable diagnosis.


