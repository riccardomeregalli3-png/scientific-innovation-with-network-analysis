\# Empirical Network Analysis and Scientific Innovation  

\## The Case of Information Theory



This repository contains the computational materials for a philosophy of science paper on the use of \*\*Empirical Network Analysis (ENA)\*\* to study \*\*scientific innovation\*\*.



The project examines whether ENA can support a general account of how scientific innovations spread across scientific communities. To do so, it applies a procedure similar to the one used by Herfeld and Doehne in their study of \*\*rational choice theory\*\* to a different case study: the diffusion of \*\*Shannon’s information theory\*\*. The aim is both reconstructive and critical: the notebook reproduces the main analytical steps of the method, while the paper discusses the philosophical significance and limitations of the results.



\## Research question



The project addresses two closely related questions:



1\. \*\*Generalizability\*\*  

&#x20;  Do the observations made by Herfeld and Doehne on the basis of the rational choice theory case generalize to a different scientific innovation?



2\. \*\*Methodological adequacy\*\*  

&#x20;  Can the topology of a citation-based network, by itself, support distinctions such as \*\*epistemic core\*\*, \*\*elaborators\*\*, and \*\*translators\*\*?



These questions are investigated through a case study of the diffusion of \*\*information theory\*\*, starting from Claude Shannon’s \*A Mathematical Theory of Communication\* (1948). :contentReference\[oaicite:2]{index=2} :contentReference\[oaicite:3]{index=3}



\## Repository contents



\- `information\_theory.ipynb`  

&#x20; Main notebook containing the computational analysis.



\- `paper/Term\_Paper\_Comp\_Methods.pdf`  

&#x20; Full paper discussing the philosophical background, the methodological choices, and the interpretation of the results.



\- `data/`  

&#x20; Input files used by the notebook, if included.



\- `requirements.txt`  

&#x20; Python dependencies needed to run the notebook.



\## What the notebook does



The notebook documents the computational part of the project. In particular, it:



1\. loads the preprocessed bibliographic data and builds the network;

2\. identifies the \*\*epistemic core\*\* using k-core decomposition;

3\. compares this result with an alternative identification based on \*\*degree centrality\*\*;

4\. detects \*\*communities\*\* using the Girvan–Newman algorithm;

5\. compares the Girvan–Newman partition with a \*\*Louvain\*\* partition using the \*\*Adjusted Rand Index (ARI)\*\*;

6\. identifies the roles of \*\*elaborators\*\* and \*\*translators\*\* on the basis of the analytical criteria discussed in the paper. :contentReference\[oaicite:4]{index=4} :contentReference\[oaicite:5]{index=5}



\## Data and network construction



The notebook starts from preprocessed CSV files. The broader data collection and preprocessing were carried out separately.



In outline, the network is derived from publications citing Shannon’s \*A Mathematical Theory of Communication\*. Bibliographic metadata were collected from \*\*Scopus\*\* and \*\*OpenAlex\*\*, filtered, and used to construct a \*\*co-citation network\*\*. Two references are connected by an edge if they are co-cited at least three times with another reference. Additional filtering steps include the exclusion of works published after 1975, the removal of edges between works published more than five years apart, and the removal of isolated nodes. The final network contains \*\*659 nodes\*\* and \*\*1,048 edges\*\*. :contentReference\[oaicite:6]{index=6}



For the full rationale behind these choices, see the accompanying paper.



\## Main findings



The case of information theory differs significantly from the rational choice theory case discussed by Herfeld and Doehne.



In particular:



\- the \*\*epistemic core\*\* emerges only at a lower k-value than in their case;

\- one cluster significantly overlaps with the epistemic core;

\- \*\*elaborators\*\* are difficult to identify using the proposed analytical criterion;

\- \*\*translators\*\* are unevenly distributed across communities;

\- the clustering results show only \*\*moderate agreement\*\* across different community-detection methods.



Taken together, these results suggest that the observations made in the rational choice theory case are not straightforwardly generalizable, and that the use of network topology to derive a general account of scientific innovation faces important methodological and conceptual difficulties. :contentReference\[oaicite:7]{index=7}





\## Requirements



The notebook relies on standard Python libraries for data handling, network analysis, and visualization, including:



\- `pandas`

\- `numpy`

\- `networkx`

\- `plotly`

\- `scikit-learn`



A `requirements.txt` file is recommended for reproducibility.



\## How to run



1\. Clone the repository.

2\. Install the required dependencies.

3\. Make sure the input data files are in the expected location.

4\. Open and run `information\_theory.ipynb`.



\## Paper



The full paper is included in the repository and provides:



\- the philosophical background on ENA and integrated history and philosophy of science;

\- the comparison with Herfeld and Doehne’s account of scientific innovation;

\- the rationale behind the construction of the network;

\- the interpretation of the results and their broader significance. :contentReference\[oaicite:8]{index=8} :contentReference\[oaicite:9]{index=9}





