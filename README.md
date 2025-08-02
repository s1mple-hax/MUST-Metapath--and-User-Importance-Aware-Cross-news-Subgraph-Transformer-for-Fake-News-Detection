# MUST: Metapath- and User Importance-Aware Cross-news Subgraph Transformer for Fake News Detection

## Datasets
To access the datasets used in this study, please use the following links and place them to the 'data' folder:

Recovery: http://coronavirus-fakenews.com

MC_Fake: https://github.com/qwerfdsaplking/MC-Fake

LIAR: https://www.cs.ucsb.edu/~william/data/liar_dataset.zip

## Requirements
python = 3.9

Cuda >= 11.8

pip install torch==2.3.0+cu118 -f https://download.pytorch.org/whl/cu118/torch/

pip install torch_geometric==2.6.1

pip install pyg_lib torch_cluster torch_scatter torch_sparse torch_spline_conv -f https://data.pyg.org/whl/torch-2.3.0+cu118.html

pip install sentence_transformers==3.4.1

pip install numpy==1.22.4

pip install scikit-learn==1.6.0

## To Run

Build heterogeneous graphs (p.s. You can adjust the TF-IDF threshold in the 'news_edge_news' function to adjust the number of news-news edges):
'''
python load_liar.py
'''

'''
python load_mc fake & recovery.py --dataset <dataset>
'''

Run MUST for fake news detection
'''
python MUST.py --dataset <dataset>
'''
