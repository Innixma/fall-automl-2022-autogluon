# Fall AutoML 2022 AutoGluon Hands-on Tutorial

[![Latest Release](https://img.shields.io/github/v/release/awslabs/autogluon)](https://github.com/awslabs/autogluon/releases)
[![Continuous Integration](https://github.com/awslabs/autogluon/actions/workflows/continuous_integration.yml/badge.svg)](https://github.com/awslabs/autogluon/actions/workflows/continuous_integration.yml)
[![Platform Tests](https://github.com/awslabs/autogluon/actions/workflows/platform_tests-command.yml/badge.svg?event=schedule)](https://github.com/awslabs/autogluon/actions/workflows/platform_tests-command.yml)
[![Python Versions](https://img.shields.io/badge/python-3.7%20%7C%203.8%20%7C%203.9-blue)](https://pypi.org/project/autogluon/)
[![GitHub license](docs/static/apache2.svg)](./LICENSE)
[![Downloads](https://pepy.tech/badge/autogluon/month)](https://pepy.tech/project/autogluon)
[![Twitter](https://img.shields.io/twitter/follow/autogluon?style=social)](https://twitter.com/autogluon)

Live Talk Recording: https://www.youtube.com/watch?v=VAAITEds-28

[Install Instructions](https://auto.gluon.ai/stable/install.html) | Documentation ([Stable](https://auto.gluon.ai/stable/index.html) | [Latest](https://auto.gluon.ai/dev/index.html))

AutoGluon automates machine learning tasks enabling you to easily achieve strong predictive performance in your applications.  With just a few lines of code, you can train and deploy high-accuracy machine learning and deep learning models on image, text, time series, and tabular data.

## Example

```python
# First install package from terminal:
# pip install -U pip
# pip install -U setuptools wheel
# pip install autogluon  # autogluon==0.5.2

from autogluon.tabular import TabularDataset, TabularPredictor
train_data = TabularDataset('https://autogluon.s3.amazonaws.com/datasets/Inc/train.csv')
test_data = TabularDataset('https://autogluon.s3.amazonaws.com/datasets/Inc/test.csv')
predictor = TabularPredictor(label='class').fit(train_data, time_limit=120)  # Fit models for 120s
leaderboard = predictor.leaderboard(test_data)
```

| AutoGluon Task      |                                                                                Quickstart                                                                                |                                                                                API                                                                                |
|:--------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| TabularPredictor    | [![Quick Start](https://img.shields.io/static/v1?label=&message=tutorial&color=grey)](https://auto.gluon.ai/stable/tutorials/tabular_prediction/tabular-quickstart.html) |                 [![API](https://img.shields.io/badge/api-reference-blue.svg)](https://auto.gluon.ai/stable/api/autogluon.predictor.html#module-0)                 |
| TextPredictor       | [![Quick Start](https://img.shields.io/static/v1?label=&message=tutorial&color=grey)](https://auto.gluon.ai/stable/tutorials/text_prediction/beginner.html)        |       [![API](https://img.shields.io/badge/api-reference-blue.svg)](https://auto.gluon.ai/stable/api/autogluon.predictor.html#autogluon.text.TextPredictor)       |
| ImagePredictor      | [![Quick Start](https://img.shields.io/static/v1?label=&message=tutorial&color=grey)](https://auto.gluon.ai/stable/tutorials/image_prediction/beginner.html)       |     [![API](https://img.shields.io/badge/api-reference-blue.svg)](https://auto.gluon.ai/stable/api/autogluon.predictor.html#autogluon.vision.ImagePredictor)      |
| ObjectDetector      | [![Quick Start](https://img.shields.io/static/v1?label=&message=tutorial&color=grey)](https://auto.gluon.ai/stable/tutorials/object_detection/beginner.html)       |     [![API](https://img.shields.io/badge/api-reference-blue.svg)](https://auto.gluon.ai/stable/api/autogluon.predictor.html#autogluon.vision.ObjectDetector)      |
| MultiModalPredictor | [![Quick Start](https://img.shields.io/static/v1?label=&message=tutorial&color=grey)](https://auto.gluon.ai/stable/tutorials/multimodal/index.html)            | [![API](https://img.shields.io/badge/api-reference-blue.svg)](https://auto.gluon.ai/stable/api/autogluon.predictor.html#autogluon.multimodal.MultiModalPredictor) |
| TimeSeriesPredictor | [![Quick Start](https://img.shields.io/static/v1?label=&message=tutorial&color=grey)](https://auto.gluon.ai/stable/tutorials/timeseries/forecasting-quickstart.html)            | [![API](https://img.shields.io/badge/api-reference-blue.svg)](https://auto.gluon.ai/stable/api/autogluon.predictor.html#autogluon.timeseries.TimeSeriesPredictor) |

## Tutorial Setup

It is recommended to use Google Colab to run the tutorials. To do so, go to the Jupyter Notebooks linked below,
go to the notebook you wish to run, and click 'Open in Colab'.

If you want to run AutoGluon locally, follow the {install instructions}.

## Tutorial Links

[AutoGluon-Tabular Tutorials](https://auto.gluon.ai/stable/tutorials/tabular_prediction/index.html)

- [Tabular Quick Start (Colab)](https://colab.research.google.com/github/gidler/autogluon-tutorials/blob/main/tutorials/tabular_prediction/tabular-quickstart.ipynb)
- [Tabular In-depth (Colab)](https://colab.research.google.com/github/gidler/autogluon-tutorials/blob/main/tutorials/tabular_prediction/tabular-indepth.ipynb)

[All Jupyter Notebooks](https://github.com/gidler/autogluon-tutorials/tree/main/tutorials)

## Extra Links

AutoGluon Website: https://auto.gluon.ai/stable/index.html

AutoGluon GitHub: https://github.com/awslabs/autogluon/

Fall AutoML School 2022 Website: https://sites.google.com/view/automl-fall-school-2022

AutoGluon-Tabular Paper: https://arxiv.org/abs/2003.06505


