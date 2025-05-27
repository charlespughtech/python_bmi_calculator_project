# BMI Calculator Project

# python_bmi_calculator_project

---

Python-based BMI Calculator implemented in a Jupyter Notebook to calculate Body Mass Index (BMI) and classify health status based on user inputs.

---

## Author

**Charles Pugh**

Google-certified Data Analyst

Email: [charlespughtech@gmail.com](mailto:charlespughtech@gmail.com)

LinkedIn: [https://www.linkedin.com/in/charlespughtech/](https://www.linkedin.com/in/charlespughtech/)

Date: May 27, 2025

---

## Table of Contents

1. [Dataset](#dataset)
2. [Requirements](#requirements)
3. [Project Structure](#project-structure)
4. [Data Cleaning](#data-cleaning)
5. [Data Analysis](#data-analysis)
6. [Usage](#usage)
7. [Contact](#contact)

---

## Dataset

The dataset for this project consists of user inputs collected interactively via the Jupyter Notebook `python_bmi_calculator_project.ipynb`. The inputs include:

- **Name**: User's name (string).
- **Weight**: User's weight in kilograms (float).
- **Height**: User's height in meters (float).

No external dataset is used. The BMI calculation and classification are based on standards from the NHS:

- **BMI Formula**: `BMI = weight (kg) / (height (m) * height (m))`
  - Source: [NHS BMI Calculator](https://www.nhs.uk/health-assessment-tools/calculate-your-body-mass-index/calculate-bmi-for-adults)
- **NHS BMI Classifications**:
  | BMI Range | Classification |
  |-----------|----------------|
  | Under 18.5 | Underweight |
  | 18.5-24.9 | Normal Weight |
  | 25-29.9 | Overweight |
  | 30-34.9 | Obese |
  | 35-39.9 | Severely Obese |
  | 40 and over | Morbidly Obese |
  - Source: [NHS Obesity Information](https://www.nhs.uk/conditions/obesity/#:~:text=Body%20mass%20index%20(BMI),-BMI%20is%20a&text=below%2018.5%20%E2%80%93%20you're%20in,re%20in%20the%20obese%20range)

---

## Requirements

- Python 3.12 or higher
- Jupyter Notebook (recommended via Anaconda or JupyterLab)
- No external libraries required (uses standard Python input/output functions)

---

## Project Structure

```bash
python_bmi_calculator_project/
├── python_bmi_calculator_project.ipynb  # Jupyter Notebook with BMI calculator code
├── python_bmi_calculator_project.html   # HTML export of the Jupyter Notebook
└── README.md                           # Project overview and instructions
```

---

## Data Cleaning

The data cleaning process is implemented within the Jupyter Notebook `python_bmi_calculator_project.ipynb` to ensure valid inputs for BMI calculation. Follow these steps to replicate:

- **Collect User Inputs and Convert Data Types**:
  - Prompt the user for their name (string), weight (kilograms), and height (meters) using `input()` functions.
  - Convert weight and height inputs to floats using `float(input(...))` to enable numerical calculations.
  - Ensure BMI calculation only proceeds for positive values (checked via `if BMI > 0`).
  - Display an error message for non-positive inputs: `"Please input numbers greater than zero."`.
- **Full Implementation**:
  - The complete code, including input collection and data type conversion, is shown below (from the notebook's final section):

```python
name = input("Enter your name: ")

weight = float(input("Enter your weight in kilograms: "))

height = float(input("Enter your height in metres: "))

print("Your name: ", name) 

print("Your weight: ", weight, "kilograms")

print("Your height: ", height, "metres")

BMI = (weight) / (height * height)

print("Your BMI: ",BMI)

if BMI > 0:
    if(BMI < 18.5):
        print("Classification: Underweight")
    elif(BMI < 25):
        print("Classification: Normal Weight")
    elif(BMI < 30):
        print("Classification: Overweight")
    elif(BMI < 35):
        print("Classification: Obese")
    elif(BMI < 40):
        print("Classification: Severely Obese")
    elif(BMI >= 40):
        print("Classification: Morbidly Obese")
    else:
        print("Please input numbers greater than zero.")
```

---

## Data Analysis

The data analysis is performed within the Jupyter Notebook using Python logic to calculate and classify BMI. Follow these steps to replicate:

- **Calculate and Classify BMI**:
  - Use the NHS formula: `BMI = weight / (height * height)`.
  - Implement conditional logic (`if/elif/else`) to categorize BMI based on NHS classifications:
    - Under 18.5: Underweight
    - 18.5–24.9: Normal Weight
    - 25–29.9: Overweight
    - 30–34.9: Obese
    - 35–39.9: Severely Obese
    - 40 and over: Morbidly Obese
- **Full Implementation**:
  - The complete code, including BMI calculation and classification, is shown below (from the notebook's final section):

```python
name = input("Enter your name: ")

weight = float(input("Enter your weight in kilograms: "))

height = float(input("Enter your height in metres: "))

print("Your name: ", name) 

print("Your weight: ", weight, "kilograms")

print("Your height: ", height, "metres")

BMI = (weight) / (height * height)

print("Your BMI: ",BMI)

if BMI > 0:
    if(BMI < 18.5):
        print("Classification: Underweight")
    elif(BMI < 25):
        print("Classification: Normal Weight")
    elif(BMI < 30):
        print("Classification: Overweight")
    elif(BMI < 35):
        print("Classification: Obese")
    elif(BMI < 40):
        print("Classification: Severely Obese")
    elif(BMI >= 40):
        print("Classification: Morbidly Obese")
    else:
        print("Please input numbers greater than zero.")
```

- **Key Insights**:
  - The program provides a personalized BMI result and health classification based on user inputs.
  - For example, a user with weight 86 kg and height 1.88 m has a BMI of approximately 24.33, classified as "Normal Weight".
  - The classification helps users understand potential health implications based on NHS standards.

---

## Usage

To explore or replicate the BMI Calculator Project, follow these steps:

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/charlespughtech/python_bmi_calculator_project.git
   cd python_bmi_calculator_project
   ```

2. **Explore the Project**:

   - Open `python_bmi_calculator_project.ipynb` in Jupyter Notebook or JupyterLab.
   - The notebook contains:
     - **Markdown Cells**: Explanations of the BMI formula, NHS classifications, and code steps, including tables for NHS BMI classifications.
     - **Code Cells**: Input collection, data type conversion, BMI calculation, and classification logic.
   - Run the notebook cells sequentially to input your name, weight, and height, and view the BMI and classification outputs.
   - Alternatively, view the static HTML export in `python_bmi_calculator_project.html` using a web browser to see the notebook content and sample outputs.

3. **Replicate the Project from Scratch** (Optional):

   - Create a new Jupyter Notebook named `python_bmi_calculator_project.ipynb`.
   - Add Markdown cells to document:
     - The BMI formula: `BMI = weight (kg) / (height (m) * height (m))`.
     - The NHS BMI classification table.
     - Sources with URLs to NHS websites.
   - Add code cells to:
     - Collect user inputs for name, weight, and height.
     - Convert weight and height to floats.
     - Calculate BMI using the formula.
     - Classify BMI using conditional statements.
     - Print personalized outputs.
   - Follow the steps in Data Cleaning and Data Analysis to implement the logic.
   - Test the notebook with sample inputs (e.g., name: "Charles", weight: 86, height: 1.88) to verify outputs match expected results (BMI ≈ 24.33, Classification: Normal Weight).
   - Export the notebook to HTML using Jupyter’s “File > Download as > HTML” to create `python_bmi_calculator_project.html`.

Results are available in `python_bmi_calculator_project.ipynb` (interactive) and `python_bmi_calculator_project.html` (static). Check the code cells for the implementation and Markdown cells for documentation.

---

## Contact

For inquiries or data analytics services, please contact:

**Charles Pugh**

Google-certified Data Analyst

Email: [charlespughtech@gmail.com](mailto:charlespughtech@gmail.com)

LinkedIn: [https://www.linkedin.com/in/charlespughtech/](https://www.linkedin.com/in/charlespughtech/)