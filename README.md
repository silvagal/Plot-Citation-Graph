# Citation Graph Visualization for Systematic Review  

This Google Colab notebook generates a citation graph based on a systematic literature review on **ECG arrhythmia classification**. The generated graph visually represents citations between papers, highlighting whether they adhere to the **interpatient data partitioning method** proposed by De Chazal et al.

## Features  
- **Graph-based visualization** of citation relationships.  
- Differentiates papers that **use** (*rounded nodes*) or **do not use** (*square nodes*) the **interpatient partitioning method** (Chazal et al.).  
- Uses data from a **CSV file** containing relevant bibliometric details.  
- Implements **PyAlex API** for citation retrieval.

## Required Setup  

1. **Set up PyAlex API access**  
   - Provide an email address to make API requests.  

2. **Upload your dataset**  
   - Prepare a **CSV file** containing the following columns:  
     - `authors` → Paper authors  
     - `title` → Paper title  
     - `abstract` → (Not used in this visualization)  
     - `cited` → List of DOIs cited by the paper  
     - `year` → Publication year  
     - `doi` → Paper DOI  
     - `chazal` → Specifies whether the paper follows the **interpatient method** (`Yes` for adherence, `No` otherwise).  
   
3. **Run the notebook**  
   - Upload your CSV file to the notebook.  
   - Execute the provided cells to generate the graph.

## Example Dataset  
A sample dataset (`example.csv`) is included in this repository, allowing users to replicate the **citation graph** shown below.

## Application  
This visualization was created for the systematic review titled:  
**"A Systematic Review of ECG Arrhythmia Classification: Embedded Feasibility, Adherence to Standards, and Fair Evaluation."**  

This graph provides insights into citation patterns and helps assess the adherence of research papers to standard evaluation practices.
