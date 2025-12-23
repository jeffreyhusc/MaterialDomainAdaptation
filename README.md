## MatDA
Code for Improving realistic material property prediction using domain adaptation based machine learning.

<b>Jeffrey Hu<sup>1</sup></b>, David Liu, Nihang Fu, Rongzhi Dong <br>

<sup>1</sup>University of Illinois Urbana-Champaign <br>
Department of Material Science and Engineering <br>

Machine Learning and Evolution Laboratory <br>
Department of Computer Science and Engineering <br>
University of South Carolina



### Cite our paper:
**Hu, Jeffrey**, David Liu, Nihang Fu, and Rongzhi Dong. Realistic material
property prediction using domain adaptation based machine learning. Dig-
ital Discovery 3, no. 2 (2024): 300-312. [PDF](https://pubs.rsc.org/en/content/articlelanding/2024/dd/d3dd00162h)

Abstract: Materials property prediction models are usually evaluated using random splitting of datasets into training and test datasets, which not only leads to over-estimated performance due to inherent redundancy, typically existent in material datasets, but also deviate from the common practice of materials scientists: they are usually interested in predicting properties for a known subset of related out-of-distribution (OOD) materials rather than universally distributed samples. Feeding such target material formulae/structures to the machine learning models should improve the prediction performance while most current machine learning (ML) models neglect this information. Here we propose to use domain adaptation (DA) to enhance current ML models for property prediction and evaluate their performance improvements in a set of five realistic application scenarios. Our systematic benchmark studies show that there exist DA models that can significantly improve the OOD test set prediction performance while standard ML models and most of the other DA techniques cannot improve or even deteriorate the performance. Our benchmark datasets and DA code can be freely accessed at https://github.com/Little-Cheryl/MatDA.

### Installation


1) Set up a virtual environment for adapting models

~~~
conda create -n adapt
conda activate adapt
pip install adapt
pip install matminer
pip install numpy==1.23
~~~

2) Set up a virtual environment for the [Modnet](https://github.com/ppdebreuck/modnet) model.


```
conda create -n modnet python=3.9
conda activate modnet
pip install modnet
```


### How to run the codes

1) As mentioned in the paper, we have 5 bandgap datasets for regression and 5 glass datasets for classification.
2) For regression problems, all codes and data are under the bandgap folder, and identical to the glass folder.
3) We separate all codes into Single and Cluster based on the dataset they use. Codes under the Single folder can be used to evaluate SparseXSingle and SparseYSingle datasets, and codes under the Cluster folder are for LOCO, SparseXCluster, and SparseYCluster.
4) Here we take the bandgap-SparseXSingle as an example:

```
cd ./bandgap/code/Single/
python adapt-RF-KMM.py
```
Users can choose the algorithms they want to evaluate, and the dataset can also be modified in each code file.

