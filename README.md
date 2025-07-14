# Shared Task on Multimodal Detection of Hate Speech, Humor, and Stance in Marginalized Socio-Political Movement Discourse at CASE 2025

[Competition Link](https://codalab.lisn.upsaclay.fr/competitions/22463) 

The complexity of text-embedded images presents a formidable challenge in machine learning, given the need for a multimodal understanding of multiple aspects of expression conveyed by them. Particularly, the marginalized movement stands as a prominent subject of online discourse, where text-embedded images like memes serve as vehicles of both solidarity and resistance, reflecting the multifaceted dynamics of attitudes and perceptions within the community and beyond. In this context, the distinction between humor and harm becomes blurred, as memes straddle the line between satire and offense, challenging researchers and platforms alike to navigate the complexities of online content moderation. As one label generally fails to encompass multiple aspects of linguistics, this shared task classifies images on four aspects: hate, targets of hate, stance, and humor as subtasks.

## Subtask A ##

**Detection of Hate Speech:** The aim is to detect the presence of hate speech in the images. The dataset for this task will have binary labels: _No Hate_ and _Hate_.

## Subtask B ##

**Classifying the Targets of Hate Speech:** Given that an image is hateful, the goal here is to identify the targets of hate speech. The dataset here will have four labels: _Undirected_, _Individual_, _Community_, and _Organization_.

## Subtask C ##

**Classification of Topical Stance:** The goal is to classify images based on their stance towards the marginalized movement. The dataset will have three labels: _Neutral_, _Support_, and _Oppose_.

## Subtask D ##

**Detection of Intended Humor:** The aim is to identify images showcasing humor, sarcasm, or satire related to the marginalized movement. The dataset for this task will have binary labels: _No Humor_ and _Humor_.

**To know more about the dataset**: please refer to our [paper](https://doi.org/10.18653/v1/2024.emnlp-main.959).

## Participation ##
Join our codalab competition [here](https://codalab.lisn.upsaclay.fr/competitions/22463).

## Dataset ## 
All the images have a unique identifier called "index". The labels for training data are organized in the folder provided. For evaluation and testing, the submission format is mentioned below.

**Training Data**

Subtask A: https://drive.google.com/drive/folders/1MX0avEqon16drjLqomwezX8_rl9_XJVC

Subtask B: https://drive.google.com/drive/folders/12GqvPap_z0RMtG7W-_s9mEXVD_pKZB48

Subtask C: https://drive.google.com/drive/folders/11aGvgClKcKJvgDoqt7EJzhajYhs0A4vd

Subtask D: https://drive.google.com/drive/folders/151BJaSNiLVMSUNvCtQJStM4tTjMo4RZa


**Evaluation Data (Without Labels)**

Subtask A: https://drive.google.com/drive/folders/1Fe-QiD_d826vX0q8a-n2-o1Q63uJfoGm

Subtask B: https://drive.google.com/drive/folders/1EN3WHaMCE0smNxIQwaFBVZ4Sb_kXtojK

Subtask C: https://drive.google.com/drive/folders/1Zovy8hcqsNFeUAUCuJIWWOsQ7TC9vpQr

Subtask D: https://drive.google.com/drive/folders/1UbukqpwOQTRQnEXyceK2Dw48ObpFqUXm

Evaluation Data Labels: https://drive.google.com/drive/folders/1DJaYJxRH7qBRwRSHXGhr1PU98HyK9sBJ

**Test Data**  
Subtask A:  
Image folder: https://drive.google.com/drive/folders/1ZjAblselR78Ns-z28XtAlq1bIQWJF_YZ?usp=sharing  
CSV file (index, text): https://drive.google.com/file/d/14D5xTWLPI7p8TeRejigQWHl4uQKZD5hT/view?usp=sharing  

Subtask B:  
Image folder: https://drive.google.com/drive/folders/1-3oNPdBOYFZWT_MhexeW_LGbgf-n0QVJ?usp=sharing  
CSV file (index, text): https://drive.google.com/file/d/1SUXpfTuGdR89D29wfwVzGvmiHJNcQKCP/view?usp=sharing  

Subtask C:  
Image folder: https://drive.google.com/drive/folders/1m2J2bfvpVvM7gC572sf0-fhfI65FSTNi?usp=sharing  
CSV file (index, text): https://drive.google.com/file/d/1a29h5QSsH5WIHg7VD3Bgp1e8KAOjE_8D/view?usp=sharing  

Subtask D:  
Image folder: https://drive.google.com/drive/folders/1W3KsuDHozn66m-zmbtvuEEAvY-sUNplP?usp=sharing   
CSV file (index, text): https://drive.google.com/file/d/1XzHE8RK1UgG9L7F_3C4jV27VyjjTvvVw/view?usp=sharing  

Test Data Labels: Available June 25, 2025

## Instructions for OCR Extraction ##
If you want to extract OCR, you can use Google Vision API, tesseract, EasyOCR, etc. In the paper that benchmarks this dataset, we have used Google Vision API to extract OCR for training the models. A lot of participants do not have access to the vision API. They can use the extracted text used in our benchmark paper.

Extracted Text for Train Data: https://drive.google.com/drive/folders/1YYUD8DxhyI3-xxq-hXSXeLpVFFaNIjN1

Extracted Text for Evaluation Data: https://drive.google.com/drive/folders/1nKn2ZiWj50eqDGHB9YEBmw5u5ArO9oIe

Extracted Text for Test Data: Refer above for CSV file (index, text) in the test data section.

## Use of External Data ##

The use of external datasets is permitted. You should also mention your external data usage in your paper write-up. A good competition-standard data that has hate speech and targets could be [CrisisHateMM dataset](https://openaccess.thecvf.com/content/CVPR2023W/MMCM/html/Bhandari_CrisisHateMM_Multimodal_Analysis_of_Directed_and_Undirected_Hate_Speech_in_CVPRW_2023_paper.html), which can be found [here](https://github.com/therealthapa/case2024-multimodal-hate). We have provided all training, evaluation, and testing datasets with labels. This data was used in shared tasks on multimodal hate speech event detection during [CASE 2023](https://aclanthology.org/2023.case-1.20/) and [CASE 2024](https://aclanthology.org/2024.case-1.31/). 

## Evaluation ## 

All the images have a unique identifier called "index". The labels for training data are organized in the folder provided. For evaluation and testing, the script takes one prediction file as input. Your submission file must be a JSON file inside a zipped archive. To submit the files, name your JSON file submission.json and zip it with the file name ref.zip. Ensure that the zip does not have any sub-directories. The system only recognizes the first file in the zip folder, so do not zip multiple files together, i.e. your ref.zip file should contain a single submission.json file. The files can have any names. The JSON file infers the label predicted by the algorithm for a specific image with a unique index.

IMPORTANT: Ensure that the index order in the submission file in JSON is in ascending order. For example:

```python

{"index": 20568.png, "prediction": 1}
{"index": 30987.png, "prediction": 0}
{"index": 45805.png, "prediction": 0}
```

<h3>Subtask A</h3>

The Non-Hate label should be assigned '0', and the Hate label should be assigned '1'. 

For example:

```python

{"index": 20568.png, "prediction": 1}
{"index": 30987.png, "prediction": 0}
{"index": 45805.png, "prediction": 0}
```

<h3>Subtask B</h3>

The Undirected label should be assigned '0', the Individual label should be assigned '1', the Community label should be assigned '2', and the Organization label should be assigned '3'.

For example:

```python

{"index": 20568.png, "prediction": 1}
{"index": 30987.png, "prediction": 0}
{"index": 45805.png, "prediction": 2}
{"index": 52125.png, "prediction": 3}

```

<h3>Subtask C</h3>

The Neutral label should be assigned '0', the Support label should be assigned '1', and the Oppose label should be assigned '2'.

For example:

```python

{"index": 20568.png, "prediction": 2}
{"index": 30987.png, "prediction": 0}
{"index": 45805.png, "prediction": 1}
```

<h3>Subtask D</h3>

The No Humor label should be assigned '0', and the Humor label should be assigned '1'. 

For example:

```python

{"index": 20568.png, "prediction": 1}
{"index": 30987.png, "prediction": 0}
{"index": 45805.png, "prediction": 0}
```

For all Subtasks, the performance will be ranked by F1 score.

To read more about the evaluation criteria, please refer to <a href="https://github.com/therealthapa/case2025-multimodal/tree/main">this page</a>.

For the hate detection task, the dataset has a balanced distribution of binary labels. The target classification task exhibits a heavily imbalanced distribution. Given the context of this study, most hateful images convey undirected hate or are targeted toward communities, with a low frequency of hate against individuals and organizations. For the stance classification task, the number of images is well-balanced across the three labels. On the other hand, as memes are often meant to be humorous, the majority of the images in the dataset are annotated as humor.

## Sample Code ##

Sample code for the dataset used in this task is available at [MemeCLIP](https://github.com/SiddhantBikram/MemeCLIP)

## Publication ##

Participants in the Shared Task are expected to submit a paper to the CASE workshop. Submitting a paper is not mandatory to participate in the shared task. Papers must follow the CASE 2025 workshop submission instructions and will undergo regular peer review. Their acceptance will not depend on the results obtained in the shared task but on the quality of the paper. All the accepted papers will be published in the ACL Anthology.

## Timeline of the Events ##
<ul>

<li>Training & Evaluation data available: April 08, 2025 </li>

<li>Test data available: May 08, 2025 </li>

<li>Testing Phase start: May 08, 2025 </li>

<li>Test end: July 12, 2025 </li>

<li>System Description Paper submissions due: July 25, 2025 </li>

<li>Notification to authors after review: August 17, 2025 </li>

<li>Revised Paper due for Conditionally Accepted Papers: August 24, 2025</li>

<li>Final Notification for Conditionally Accepted Papers: August 25, 2025</li>

<li>Camera ready: August 30, 2025 </li>

<li>CASE Workshop: September 11-13, 2025 </li>


</ul>

## Organizers ##
<ul>
<li> Surendrabikram Thapa (Virginia Tech, USA) </li>
<li> Siddhant Bikram Shah (Northeastern University, USA) </li>
<li> Shuvam Shiwakoti (Virginia Tech, USA) </li>
<li> Kritesh Rauniyar (Delhi Technological University, India) </li>
<li> Surabhi Adhikari (Columbia University, USA) </li>
<li> Hariram Veeramani (UCLA, USA) </li>
<li> Kristina T. Johnson (Northeastern University, USA) </li>
<li> Hristo Tanev (European Commission, Joint Research Centre (EU JRC) </li>
<li> Ali Hürriyetoğlu (KNAW Humanities Cluster DHLab, Netherlands) </li>
<li> Usman Naseem (Macquarie University, Australia) </li>
</ul>

## Contact ##
If there are any questions related to the competition, please contact rauniyark11@gmail.com

## References ##
Will be provided later.

## Anti-Harassment policy ##

We uphold the [ACL Anti-Harassment Policy](https://www.aclweb.org/adminwiki/index.php?title=Anti-Harassment_Policy), and participants in this shared task are encouraged to reach out with any concerns or questions to any of the shared task organizers.
