# Web Traffic Prediction via Temporal Graph Neural Network


 <div align="center">
    <a href="https://colab.research.google.com/github/reshalfahsi/web-traffic-prediction/blob/master/Web_Traffic_Prediction.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="colab"></a>
    <br />
 </div>


Temporal Graph Neural Network or Temporal GNN is one of the variant of the GNN which handles the spatio-temporal data. The term "spatio-" refers to the nature of the graph that is closely related to the spatial relationship that exists in the image data (recall that an image is basically a graph), and the term "temporal" here indicates the data may be progressively changing in a sequence of time. In this project, the [Chebysev GCNN+LSTM](https://arxiv.org/pdf/1612.07659.pdf) module and the Wiki Maths dataset are leveraged, which are provided by [PyTorch Geometric Temporal](https://github.com/benedekrozemberczki/pytorch_geometric_temporal). The complete Temporal GNN model contains the Chebysev GCNN+LSTM module, followed by MLP. Here, the model is trained to predict the daily user visits to Wikipedia's vital mathematics articles (represented by nodes/vertices). The graph's characteristic in the dataset is non-heterogenous and static. The details of the dataset can be seen [here](https://pytorch-geometric-temporal.readthedocs.io/en/latest/modules/dataset.html#torch_geometric_temporal.dataset.wikimath.WikiMathsDatasetLoader). 


## Experiment


To try out the experiment, the [Google Colab notebook]((https://github.com/reshalfahsi/web-traffic-prediction/blob/master/Web_Traffic_Prediction.ipynb) is provided.


## Result

## Quantitative Result

The quantitative performance of the model is given in the table below.

Metrics | Score |
------------ | ------------- |
Loss | 0.452 |
MAPE | 4.110 |
MAE | 0.438 |
MSE | 0.519 |



## Evaluation Metric Curve

<p align="center"> <img src="https://github.com/reshalfahsi/web-traffic-prediction/blob/master/assets/loss_curve.png" alt="loss_curve" > <br /> Loss curve of the training and validation of the Temporal GNN model. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/web-traffic-prediction/blob/master/assets/mape_curve.png" alt="mape_curve" > <br /> MAPE curve of the training and validation of the Temporal GNN model. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/web-traffic-prediction/blob/master/assets/mae_curve.png" alt="mae_curve" > <br /> MAE curve of the training and validation of the Temporal GNN model. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/web-traffic-prediction/blob/master/assets/mse_curve.png" alt="mse_curve" > <br /> MSE curve of the training and validation of the Temporal GNN model. </p>


## Qualitative Result

The figure below shows the qualitative result of the model.

<p align="center"> <img src="https://github.com/reshalfahsi/web-traffic-prediction/blob/master/assets/qualitative_result.png" alt="qualitative_result" > <br /> The visitor prediction at one of the vital mathematics articles on Wikipedia. </p>


## Credit

- [Structured Sequence Modeling with Graph Convolutional Recurrent Networks](https://arxiv.org/pdf/1612.07659.pdf)
- [PyTorch Geometric Temporal](https://github.com/benedekrozemberczki/pytorch_geometric_temporal)
- [PyTorch Lightning](https://lightning.ai/docs/pytorch/latest/)
