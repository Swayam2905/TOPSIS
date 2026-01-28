**TOPSIS Implementation in Python**

This project implements the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) method using Python.
TOPSIS is a multi-criteria decision-making technique used to rank alternatives based on their distance from an ideal best and ideal worst solution.

**📌 Features**

Accepts input data in CSV format

Supports custom weights and impacts

Automatically calculates:

Normalized matrix

Weighted normalized matrix

TOPSIS score

Rank of each alternative

Generates output as a CSV file

📂 Project Structure
.
├── topsis.py
├── input_topsis.csv
├── output.csv
└── README.md

**📥 Input File Format**

The input file must be a CSV file where:

The first column contains the names of alternatives

The remaining columns contain numerical criteria values

Example: input_topsis.csv
Fund Name,P1,P2,P3,P4,P5
M1,0.84,0.71,6.7,42.1,12.59
M2,0.91,0.83,7.0,31.7,10.11
M3,0.79,0.62,4.8,46.7,13.23
M4,0.78,0.61,6.4,42.4,12.55
M5,0.94,0.88,3.6,62.2,16.91

**⚙️ How to Run the Code**
1️⃣ Install Required Libraries

Make sure Python is installed, then run:

pip install pandas numpy

2️⃣ Run the Program
python topsis.py

🧪 Parameters Used

Inside the code, the function is called as:

topsis(
    input_file="input_topsis.csv",
    weights_str="1,1,1,1,1",
    impacts_str="+,+,+,-,+",
    output_file="output.csv"
)


weights_str: Importance of each criterion

impacts_str:

+ → Higher value is better

- → Lower value is better

**📤 Output File**

The output file (output.csv) contains:

Topsis Score

Rank (1 = Best alternative)

Example Output
Fund Name,P1,P2,P3,P4,P5,Topsis Score,Rank
M2,0.91,0.83,7.0,31.7,10.11,0.7821,1
M5,0.94,0.88,3.6,62.2,16.91,0.6213,2
...

**📚 About TOPSIS**

TOPSIS ranks alternatives based on:

Minimum distance from the ideal best solution

Maximum distance from the ideal worst solution

It is widely used in:

Decision making

Engineering selection problems

Finance and investment analysis

Management science

**👤 Author**

Swayam Gupta
