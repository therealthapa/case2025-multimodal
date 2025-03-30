# Shared Task on Multimodal Detection of Hate Speech, Humor, and Stance in LGBTQ+ Socio-Political Movement Discourse at CASE 2025

The complexity of text-embedded images presents a formidable challenge in ML given the need for multimodal understanding of multiple aspects of expression conveyed by them. Particularly, the LGBTQ+ movement stands as a prominent subject of online discourse, where text-embedded images like memes serve as vehicles of both solidarity and resistance, reflecting the multifaceted dynamics of attitudes and perceptions within the community and beyond. In this context, the distinction between humor and harm becomes blurred, as memes straddle the line between satire and offense, challenging researchers and platforms alike to navigate the complexities of online content moderation. As one label generally fails to encompass multiple aspects of linguistics, this shared task classifies images on four aspects: hate, targets of hate, stance, and humor as subtasks.

## Sub-task 1 ##

**Detection of Hate Speech:** The aim is to detect the presence of hate speech in the images. The dataset for this task will have binary labels: _No Hate_ and _Hate_.

## Sub-task 2 ##

**Classifying the Targets of Hate Speech:** Given that an image is hateful, the goal here is to identify the targets of hate speech. The dataset here will have four labels: _Undirected_, _Individual_, _Community_, and _Organization_.

## Sub-task 3 ##

**Classification of Topical Stance:** The goal is to classify images based on their stance towards the LGBTQ+ movement. The dataset will have three labels: _Neutral_, _Support_, and _Oppose_.

## Sub-task 4 ##

**Detection of Intended Humor:** The aim is to identify images showcasing humor, sarcasm, or satire related to the LGBTQ+ Pride movement. The dataset for this task will have binary labels: _No Humor_ and _Humor_.

## Participation ##
Join our codalab competition here.

## Dataset ## 
All the images have a unique identifier called "index". The labels for training data are organized in the folder provided. For evaluation and testing, the submission format is mentioned below.

Training Data
Subtask A:
Subtask B: 
Subtask C:
Subtask D:

Evaluation Data (Without Labels)
Subtask A:
Subtask B: 
Subtask C:
Subtask D:

Evaluation Data Labels: 

Test Data
Subtask A: Available May 05, 2025
Subtask B: Available May 05, 2025
Subtask C: Available May 05, 2025
Subtask D: Available May 05, 2025

Test Data Labels: Available June 25, 2025

## Instructions for OCR Extraction ##
If you want to extract OCR, you can use Google Vision API, tesseract, EasyOCR, etc. In the paper that benchmarks this dataset, we have used Google Vision API to extract OCR for training the models. A lot of participants do not have access to the vision API. They can use the extracted text used in our benchmark paper from ______. 

## Evaluation ## 

All the images have a unique identifier called "index". The labels for training data are organized in the folder provided. For evaluation and testing, the script takes one prediction file as input. Your submission file must be a JSON file inside a zipped archive. To submit the files, name your JSON file submission.json and zip it with the file name ref.zip. Ensure that the zip does not have any sub-directories. The system only recognizes the first file in the zip folder, so do not zip multiple files together, i.e. your ref.zip file should contain a single submission.json file. The files can have any names. The JSON file infers the label predicted by the algorithm for a specific image with a unique index.

A sample file is available at X.

IMPORTANT: Ensure that the index order in the submission file in JSON is in ascending order. For example:

```python

{"index": 20568, "prediction": 1}
{"index": 30987, "prediction": 0}
{"index": 45805, "prediction": 0}
```

<h3>Subtask 1</h3>

The Non-Hate label should be assigned '0', and the Hate label should be assigned '1'. 

<h3>Subtask 2</h3>

The Undirected label should be assigned '0', the Individual label should be assigned '1', the Community label should be assigned '2', and the Organization label should be assigned '3'.

<h3>Subtask 3</h3>

The Neutral label should be assigned '0', the Support label should be assigned '1', and the Oppose label should be assigned '3'.

<h3>Subtask 4</h3>

The No Humor label should be assigned '0', and the Humor label should be assigned '1'. 

For all Subtasks, the performance will be ranked by F1 score.

To read more about the evaluation criteria, please refer to <a href="https://github.com/therealthapa/case2025-multimodal/tree/main">this page</a>.

For the hate detection task, the dataset has a balanced distribution of binary labels. The target classification task exhibits a heavily imbalanced distribution. Given the context of this study, most hateful images convey undirected hate or are targeted toward communities, with a low frequency of hate against individuals and organizations. For the stance classification task, the number of images is well-balanced across the three labels. On the other hand, as memes are often meant to be humorous, the majority of the images in the dataset are annotated as humor.

## Publication ##

Participants in the Shared Task are expected to submit a paper to the CASE workshop. Submitting a paper is not mandatory for participating in the Shared Task. Papers must follow the CASE 2025 workshop submission instructions and will undergo regular peer review. Their acceptance will not depend on the results obtained in the shared task but on the quality of the paper. Authors of accepted papers will be informed about the evaluation results of their systems prior to the paper submission deadline (see the important dates). All the accepted papers will be published in ACL Anthology.

## Timeline of the Events ##
<ul>

<li>Training & Evaluation data available: April 4, 2025 </li>

<li>Test data available: May 05, 2025 </li>

<li>Testing Phase start: May 05, 2025 </li>

<li>Test end: June 25, 2025 </li>

<li>System Description Paper submissions due: July 10, 2025 </li>

<li>Notification to authors after review: August 10, 2025 </li>

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
<li> Kristina T. Johnson (Northeastern University, USA) </li>
<li> Hristo Tanev (European Commission, Joint Research Centre (EU JRC) </li>
<li> Ali Hürriyetoğlu (KNAW Humanities Cluster DHLab, Netherlands) </li>
<li> Usman Naseem (Macquarie University, Australia) </li>
</ul>

## Contact ##
If there are any questions related to the competition, please contact shuvam@vt.edu 

## References ##
Will be provided later.


