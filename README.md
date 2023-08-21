
# Knowledge-based Version Incompatibility Detection for Deep Learning

This repository contains data and code to build DECIDE, a version incompatibility detection tool based on pre-trained language models proposed in *"Knowledge-based Version Incompatibility Detection for Deep Learning"*. Meanwhile, this repository also contains data and code to replicate experiment results in the paper. This repository has been made publicly available on GitHub^[put your github link here] to support Open Science. The remaining of this README file explains how to replicate experiment results from the paper by research questions.

## Docker Installation
Before the experiment results can be replicated, please read the instructions on how to build the docker container (**install.md**) that contain necessary code and data to run DECIDE. All operations should be made in the docker container command line.


### RQ1: How effectively can  DECIDE detect version compatibility issues in real DL projects?
To evaluate the performance of DECIDE, we compare DECIDE against two state-of-the-art baselines: Watchman^[Ying Wang, Ming Wen, Yepang Liu, Yibo Wang, Zhenming Li, Chao Wang,  
Hai Yu, Shing-Chi Cheung, Chang Xu, and Zhiliang Zhu. 2020.  Watchman:  
Monitoring Dependency Conflicts for Python Library Ecosystem. In  Proceedings  
of the ACM/IEEE 42nd International Conference on Software Engineering  (Seoul,  
South Korea)  (ICSE ’20). Association for Computing Machinery, New York, NY,  
USA, 125–135.] and PyEGo^[Hongjie Ye, Wei Chen, Wensheng Dou, Guoquan Wu, and Jun Wei. 2022.  
Knowledge-Based Environment Dependency Inference for Python Programs.  
In  2022 IEEE/ACM 44th International Conference on Software Engineering (ICSE).  
1245–1256.] on  a benchmark consisting of 10 popular DL projects from GitHub (`/data`).  Figure 6 in the paper shows the number of version issuess detected by DECIDE, PyEGo, and Watchman on different DL stack layers. To reproduce the result, run:
`blahblahblah`

Furthermore, Table 6 shows the accuracy of version incompatability detection of the three approaches in terms of precision, recall, and F1 score. To reproduce Table 6, run:
`blahblahblah`

### RQ2: How accurate is the extracted knowledge in the resulting knowledge graph produced by DECIDE ?
The intermediate output of DECIDE is a knowledge graph that contain 3,124 relations in the knowledge graph. To evaluate the accuracy of the extracted knowledge in the knowledge graph, we randomly sampled 343 version (in)compatibility relations. The accuracy of the sampled relations is **0.89**. To reproduce this result, run:
`blahblahblah`

### RQ3: How accurately can the pre-trained QA model in  DECIDE infer compatibility relations between versioned DL components?
To construct the knowledge graph, DECIDE uses UnifiedQA, a pretrained QA model to extract (in)compatibility relations from Stack Overflow posts. To evaluate the accuracy of UnifiedQA, we randomly sampled 360 of the 5,532 queries it received during the construction of the knowledge graph. We compared the inference results of UnifiedQA against the human-annotated groundtruth and found that UnifiedQA achieved 84.2% precision and 91.3% recall on these 360 queries. To reproduce this result, run: 
`blahblahblah`

### RQ4: To what extent can different question templates affect the accuracy of the pre-trained QA model in DECIDE?
When prompting UnifiedQA to infer (in)compatibility relations from Stack Overflow posts, we design eight prompt templates (Table 4). Table 7 from the paper shows the model accuracy when using different question templates. To reproduce this result, run:
`blahblahblah`

Furthermore, we also experimented with different combinations of prompt templates and showed the results in Table 8 in the paper. To reproduce Table 8, run:
`blahblahblah`

### RQQ5: To what extent can different knowledge consolidation strategies affect the accuracy of the resulting knowledge graph?
To  eliminate redundancies and reconcile conflicts in the knowledge graph, we developed three different knowledge consolidation strategies (*majority vote*, *weighted majority vote*, and *vote by loss*). We randomly sampled the 228 relations with conflicts to test each consolidation method. The results showed that the majority vote strategy achieves the best accuracy, 95.1%, followed by voting by loss  (93.6%) and weighted majority vote (91.6%). To reproduce this result, run:
`blahblahblah`
