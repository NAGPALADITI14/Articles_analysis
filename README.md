# Articles_analysis: Text Extraction, Cleaning, and Analysis  

This project systematically processes a set of URLs provided in an Excel sheet to extract, analyze, and summarize textual content. The approach involves several key steps, including article extraction, word list loading, text analysis, and generating structured outputs.

---

## 🚀 **Approach Used for the Solution**  

### 1. **Extracting Articles**  
- Read the input Excel sheet (`Input.xlsx`) containing `URL_ID` and `URL` columns.  
- For each URL:  
  - Fetch the web content using the `requests` library.  
  - Parse the HTML using the `BeautifulSoup` library to extract the **title** and main content (from specific HTML tags).  
  - Save the extracted content as individual text files, named according to their `URL_ID`.  

### 2. **Loading Word Lists**  
- Load predefined **positive**, **negative**, and **stopword** lists from text files.  
- Use the `chardet` library to detect the encoding of the word list files for accurate reading.  
- Normalize all words to lowercase and remove extra spaces for consistency.  

### 3. **Text Analysis**  
- Tokenize text into words and sentences using the `nltk` library.  
- Filter out stopwords and non-alphabetic tokens.  
- Calculate the following metrics:  
  - **Positive Score** and **Negative Score** using the respective dictionaries.  
  - **Polarity** and **Subjectivity Scores** to assess the overall tone.  
  - **Readability Metrics**:  
    - Average sentence length.  
    - Percentage of complex words (words with two or more syllables).  
    - **Fog Index** to measure readability.  
  - **Additional Metrics**:  
    - Word count.  
    - Syllables per word.  
    - Average word length.  
    - Number of personal pronouns.  

### 4. **Generating Output**  
- Consolidate results into a structured format.  
- Save the output as an Excel sheet (`OutputDataStructure.xlsx`) containing all calculated metrics.  

---

## 🛠️ **How to Run the Python Script**  

### 1. **Setup**  

#### Install Required Libraries  
Run the following command in your terminal or command prompt to install the necessary libraries:  
```bash
pip install pandas requests beautifulsoup4 chardet nltk textstat

#### 2. **Prepare Files and Folders**
Place the input Excel sheet (Input.xlsx) containing URL_ID and URL columns in the working directory.
Ensure the word list filenames and folder names do not contain extra spaces.
#### 3. **Run the Script**
###Preferred Method: Google Colab
Upload the script and required files to Google Colab.
Execute the cells sequentially in the notebook.
###Alternative: Local Environment
Save the script as analyze_articles.py.
Run the script using the command:

### 📦 **Dependencies Required**
Python Libraries:
-pandas: For handling and processing Excel sheets.
-requests: To fetch web content from URLs.
-beautifulsoup4: To parse and extract HTML content.
-chardet: To detect file encodings.
-nltk: For tokenizing text into words and sentences.
-textstat: For calculating syllables and Fog Index.
### 1. **Setup**  

#### Install Required Libraries  
Run the following command in your terminal or command prompt to install the necessary libraries:  
```bash
pip install pandas requests beautifulsoup4 chardet nltk textstat
