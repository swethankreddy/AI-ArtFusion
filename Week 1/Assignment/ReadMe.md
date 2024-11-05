# ArtFusion: Where Art Meets AI

## Project Overview
ArtFusion is an innovative project that combines artificial intelligence with artistic expression by transforming ordinary images into stunning works of art using neural style transfer. This hands-on project provides a practical introduction to machine learning concepts, allowing you to create a portfolio of unique, AI-enhanced creations.

## Week 1 Assignments: Topic-Focused

### Assignment 1: Python Installation and Environment Setup
1. **Objective**: Set up a Python development environment and ensure all necessary tools are ready for coding.
2. **Instructions for Installing Python**:
   - **Windows**:
     1. Download the latest Python installer from the [official Python website](https://www.python.org/downloads/).
     2. Run the installer and ensure you check the box that says "Add Python to PATH."
     3. Follow the installation prompts.
   - **macOS**:
     1. You can use Homebrew to install Python. Open your terminal and run:
        ```bash
        brew install python
        ```
     2. Alternatively, download the installer from the [official Python website](https://www.python.org/downloads/) and follow the installation instructions.
   - **Linux**:
     1. Use the package manager for your distribution. For example, on Ubuntu, you can run:
        ```bash
        sudo apt update
        sudo apt install python3
        ```
3. **Set Up a Virtual Environment (Optional)**:
   - If you choose to use a virtual environment, install the virtualenv package:
     ```bash
     pip install virtualenv
     ```
   - Create a virtual environment:
     ```bash
     virtualenv artfusion_env
     ```
   - Activate the virtual environment:
     - On Windows:
       ```bash
       artfusion_env\Scripts\activate
       ```
     - On macOS/Linux:
       ```bash
       source artfusion_env/bin/activate
       ```
4. **Install Jupyter Notebook and Required Libraries**:
   - Install Jupyter Notebook and necessary libraries:
     ```bash
     pip install notebook numpy pandas matplotlib tensorflow
     ```
5. **Launch Jupyter Notebook**: Create a new Python notebook titled `Week1_Introduction.ipynb`.
6. **Deliverable**: A screenshot of your Jupyter Notebook environment with the notebook open, along with a brief summary of the benefits of using a virtual environment for this project.

### Assignment 2: Basic Python Functions and Data Structures
1. **Objective**: Reinforce Python fundamentals with practical applications relevant to data processing.
2. **Topics Covered**: Basic data types, functions, loops, and conditionals.
3. **Tasks**:
   - Create a Python script or Jupyter Notebook that includes the following:
     1. **Function Definitions**:
        - Write a function `calculate_area(radius)` that returns the area of a circle given its radius.
        - Write a function `is_prime(num)` that checks whether a number is prime.
     2. **Loops and Conditionals**:
        - Create a list of integers from 1 to 50. Use a loop to print all prime numbers from this list.
        - Generate a list of squares of the first 10 integers and print the list.
4. **Deliverable**: Submit your Python script or Jupyter Notebook with all functions and results, including comments explaining your code.

---

### Assignment 3: Data Manipulation with NumPy
1. **Objective**: Gain practical experience with NumPy for numerical computations.
2. **Topics Covered**: NumPy arrays, basic operations, indexing, and slicing.
3. **Tasks**:
   - Install NumPy if you haven't already:
     ```bash
     pip install numpy
     ```
   - In your Jupyter Notebook, perform the following tasks:
     1. Create a 1D NumPy array of 20 random integers between 1 and 100.
     2. Compute the following:
        - Mean, median, and standard deviation of the array.
        - Create a new array containing only the even numbers from the original array.
     3. Create a 2D NumPy array (5x4) of random integers and demonstrate how to slice it to obtain the first three rows.
4. **Deliverable**: Submit your completed Jupyter Notebook showing all calculations, array creations, and explanations for each step.

---

### Assignment 4: Data Analysis with Pandas
1. **Objective**: Learn to use Pandas for data analysis and manipulation.
2. **Topics Covered**: DataFrames, basic operations, filtering, and visualizations.
3. **Tasks**:
   - Install Pandas:
     ```bash
     pip install pandas
     ```
   - Load a CSV dataset of your choice (e.g., Iris dataset) using Pandas.
   - Perform the following tasks:
     1. Display the first five rows of the dataset and summarize the structure (data types, missing values).
     2. Calculate basic statistics (mean, median, count) for numeric columns.
     3. Filter the dataset to show only rows that meet a specific condition (e.g., sepal length > 5.0) and visualize the distribution of one of the features using a histogram.
4. **Deliverable**: Submit your completed Jupyter Notebook with data analysis steps, visualizations, and interpretations.
