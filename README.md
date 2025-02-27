# Citation Graph Visualization for Systematic Review  

This Google Colab notebook generates a **directed citation graph** based on a systematic literature review on **ECG arrhythmia classification**. The graph visually represents citation relationships, where **arrows originate from the citing article and point to the cited article**.  

## Features  
- **Graph-based visualization** of citation relationships.  
- **Directed edges**: Arrows indicate the citation flow from one article to another.  
- **Node size**: The larger the node, the more papers within the review have cited that article.  
- **Color scale**: Represents the total number of citations the article has in the broader literature (not just within the review).  
- Differentiates papers that **use** (*rounded nodes*) or **do not use** (*square nodes*) the **interpatient partitioning method** Chazal et al. (2004).  
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

This graph provides insights into citation patterns, helping to assess research influence and adherence to standard evaluation practices.

![Citation Graph](ecg_citation_graph.png)

## References  
De Chazal, P., O'Dwyer, M., & Reilly, R. B. (2004). Automatic classification of heartbeats using ECG morphology and heartbeat interval features. *IEEE Transactions on Biomedical Engineering, 51*(7), 1196-1206. [DOI: 10.1109/TBME.2004.827359](https://doi.org/10.1109/TBME.2004.827359)

