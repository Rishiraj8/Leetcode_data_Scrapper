Here's a `README.md` file tailored for your script, explaining its purpose, usage, and contributions:

---

# LeetCode Data Scraping Tool for Student Performance Monitoring  

## Overview  
This Python script is designed to collect LeetCode performance data for students in a structured manner. It retrieves statistics like problem-solving counts, contest participation, and ratings using the LeetCode GraphQL API. The scraped data is compiled into an Excel sheet, making it easy for institutions to monitor and evaluate students' coding progress and engagement.

## Purpose  
Developed as a contribution to **[Your Institution Name]**, this tool helps faculty and administrators:  
1. Monitor students' coding proficiency.  
2. Track problem-solving progress across Easy, Medium, and Hard difficulties.  
3. Evaluate contest participation and ratings.  
4. Encourage competitive programming within the institution.  

This script is currently used by the institution as a free and efficient tool for data scraping and reporting.

---

## Features  
- **Automated Data Fetching**: Retrieves individual student data using LeetCode's public GraphQL API.  
- **Excel Report Generation**: Compiles data into a clean Excel sheet for easy analysis.  
- **Error Handling**: Skips and reports rows with invalid or missing data without stopping the script.  
- **Customizable**: Can be adapted for other data fields or APIs if needed.  

---

## Data Collected  
The following information is retrieved for each student:  
1. **Easy Solved**: Number of easy-level problems solved.  
2. **Medium Solved**: Number of medium-level problems solved.  
3. **Hard Solved**: Number of hard-level problems solved.  
4. **Attended Contests Count**: Number of contests the student has participated in.  
5. **Rating**: The student's contest rating.  

The output Excel sheet includes the following columns:  
- S. No  
- Roll No  
- Name  
- Class  
- LeetCode ID  
- LeetCode Profile Link  
- Easy Solved  
- Medium Solved  
- Hard Solved  
- Attended Contests Count  
- Rating  

---

## Prerequisites  
To run the script, ensure you have the following installed:  
1. Python 3.x  
2. Libraries:  
   - `requests`  
   - `openpyxl`  
   - `json`  
3. Google Colab (if running in a notebook environment).  

---

## How to Use  

### Step 1: Prepare Input Excel File  
The input Excel file should include student details with the following format:  
| S No | Roll No | Name | Class | LeetCode ID | LeetCode Profile Link |  
|------|---------|------|-------|-------------|-----------------------|  

Ensure the "LeetCode ID" column contains valid usernames.

### Step 2: Run the Script  
- Upload the prepared Excel file when prompted.  
- The script fetches data for each student and compiles it into a new Excel file named `LeetCode_Rishi.xlsx`.  
- Download the generated Excel file.  

### Step 3: Analyze the Results  
Open the output file and review the students' LeetCode performance. Missing or incorrect data is marked with "Error" or "Id Wrong."

---

## Error Handling  
- Rows with incomplete or invalid data are skipped and logged with an error message.  
- Any failure in the LeetCode API call will result in "Error" entries for the respective student.  

---

## Code Explanation  

1. **LeetCode API Queries**  
   - Fetches **contest ranking** and **problem-solving stats** using GraphQL queries.  

2. **Input and Output**  
   - Reads the input Excel file.  
   - Writes the fetched data into a new Excel sheet.  

3. **Error Management**  
   - Handles API failures, missing data, or incorrect LeetCode IDs.  

4. **Rate-Limiting**  
   - Includes a `time.sleep(1)` delay between requests to avoid being rate-limited.  

---

## Contributions  
This tool was developed by **[Your Name]** as a contribution to **[Your Institution Name]**. It is designed to help track and enhance students' coding performance effectively and efficiently.  

---

## License  
This tool is open for educational purposes within **[Your Institution Name]**. Any use beyond this requires appropriate credits to the contributor.

---

### Future Enhancements  
- Support for additional coding platforms (e.g., Codeforces, CodeChef).  
- Visualization of data using charts or graphs.  

---

**Author**: [Your Name]  
**Institution**: [Your Institution Name]  
**Contact**: [Your Email]  

--- 

Let me know if you need any changes or additional sections! 🚀
