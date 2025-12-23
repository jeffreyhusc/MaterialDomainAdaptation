## MatDA
Code for Improving realistic material property prediction using domain adaptation based machine learning.

### Cite our paper:
**Hu, Jeffrey**, David Liu, Nihang Fu, and Rongzhi Dong. Realistic material
property prediction using domain adaptation based machine learning. Dig-
ital Discovery 3, no. 2 (2024): 300-312. [PDF](https://pubs.rsc.org/en/content/articlelanding/2024/dd/d3dd00162h)

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

