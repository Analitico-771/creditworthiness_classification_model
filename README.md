
<!-- Find and Replace All [repo_name] -->
<!-- Replace [product-screenshot] [product-url] -->
<!-- Other Badgets https://naereen.github.io/badges/ -->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![LinkedIn][linkedin-shield]][linkedin-url]
<!-- [![License][license-shield]][license-url] -->


<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <!-- <a href="#overview-of-the-analysis">Overview of the Analysis</a> -->
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#overview-of-the-analysis">Overview of the Analysis</a>
    </li>
    <li>
      <a href="#results">Results</a>
    </li>
    <li>
      <a href="#summary">Summary</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
	<!-- <li><a href="#license">License</a></li> -->
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About The Project

This is an Application that trains a model using supervised learning and imbalanced-learn library in order to classify and identify the creditworthiness of borrowers.

### Built With

<!-- This section should list any major frameworks that you built your project using. Leave any add-ons/plugins for the acknowledgements section. Here are a few examples. -->

* [Python](https://www.python.org/)
* [Python CSV Reading/Writing](https://docs.python.org/3/library/csv.html)
* [Python pandas](https://pandas.pydata.org/)
* [Python scikit-learn](https://scikit-learn.org/stable/)
* [Python conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html)
* [Python JupyterLab](https://jupyter.org/)

## Overview of the Analysis

* The purpose of the analysis is to train a model that can classify and identify the creditworthiness of borrowers
* The dataset is of historical lending activity from a peer-to-peer lending services company, and what you are trying to predict are the people who are likely to default on a loan.
* The variables that is being predicted is the `y_prediction`.  I start with the `y_variable` which holds the values of the `loan_status` column and use the `value_counts` method to see the count of good and bad loans in the dataset. I use this information to build the test data for training and prediction.
* I build two models and used `LogisticRegression` method on one, and `RandomOverSampler` on the other.

## Results

* Machine Learning Model 1 `LogisticRegression`:
  * `balanced_accuracy_score` = 0.9520479254722232
  * `precision`  0=1.00,  1=0.85
  * `recall`     0=0.99,  1=0.91

* Machine Learning Model 2 `RandomOverSampler`:
  * `balanced_accuracy_score` = 0.9947308560359689
  * `precision`  0=0.99,  1=0.99
  * `recall`     0=0.99,  1=0.99

## Summary

* The `RandomOverSampler` seems to perform best because it detects more of the potential people who are likely to default on loans based on their credit risk.
* Thee performance depends on the problem you are trying to solve.  Here I'm not concerned about overclassifying the good loans because that's a good thing.  I'm more concerned about increasing the 1's classification.

I only recommend the `RandomOverSampler` model is used for this problem.

<!-- GETTING STARTED -->
## Getting Started

<!-- This is an example of how you may give instructions on setting up your project locally. To get a local copy up and running follow these simple example steps. -->
* Install and import the required libraries and dependencies ONLY as needed!

* You don't need Python installed in your computer. You can install Anaconda and JupyterLab normally just like any other application on your computer. Follow the instructions for Anaconda, ensure that its working, then install JupyterLab.

* I have placed Comments throughout the code so that you can follow the code and be able to replicate the app on your own. Also, so that you're able to contribute in the future :-)

### Prerequisites

<!-- This is an example of how to list things you need to use the software and how to install them. -->
A text editor such as [VS Code](https://code.visualstudio.com/) or [Sublime Text](https://www.sublimetext.com/)


### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/AnaIitico/creditworthiness_classification_model.git
   ```

2. You don't need to install pip - Conda comes with pip and you can also use the command
    conda install 'package name'
   
3. Install Conda according to the instructions based on your operating system.
    For windows users you MUST use the Administrator PowerShell. Users with AMD Processors MUST use the Administrator PowerShell 7 (X64) version
  
    Once installed Conda has an Admin PowerShell version shortcut - look on your Start menu for it.
    This shortcut will prove very useful at times when you need to install other apps or make adjustments to your installation

    Once installed you will see (base) on your terminal
   
4. Activate Conda Dev environment
   ```sh
   conda activate dev
   ```
   You should now see (dev) on your terminal

5. Install JupyterLabs
   ```sh
   pip install jupyterlab
   ```

6. Run JupyterLabs
   ```sh
   jupyter lab
   ```
   A browser window should open on localhost:8888/lab

<!-- USAGE EXAMPLES -->
## Usage
  
<!-- Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources. -->

<!-- ROADMAP -->

## Roadmap

  The app is finished
<!-- Here are some screenshots and code snippets of the working app

#### Exchange Comparison January 2018
![Exchange January Screen Shot][exchange-january-screenshot]

#### Exchange Comparison March 2018 - With Analysis
![Exchange March Screen Shot][exchange-march-screenshot]


#### Calculate Arbitrage Profits Snippet - for January 16 only
#### you can see the full code (with outputs) in the [crypto_arbitrage.ipynb](https://github.com/AnaIitico/creditworthiness_classification_model/blob/main/crypto_arbitrage.ipynb) file
  *This code has been summarized into one block for convenience*
  *and there's an analysis at the end*
```sh
  # some cool code here
 ``` -->

See the [open issues](https://github.com/AnaIitico/creditworthiness_classification_model/issues) for a list of proposed features (and known issues).

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<!-- LICENSE -->
<!-- ## License

Distributed under the MIT License. See `LICENSE` for more information.
 -->

<!-- CONTACT -->
## Contact

Jose Tollinchi - [@josetollinchi][linkedin-url] - jtollinchi1971@gmail.com

Project Link: [https://github.com/AnaIitico/creditworthiness_classification_model](https://github.com/AnaIitico/creditworthiness_classification_model)

<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

* [Img Shields](https://shields.io)
* [Choose an Open Source License](https://choosealicense.com)

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/AnaIitico/creditworthiness_classification_model.svg?style=for-the-badge
[contributors-url]: https://github.com/AnaIitico/creditworthiness_classification_model/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/AnaIitico/creditworthiness_classification_model.svg?style=for-the-badge
[forks-url]: https://github.com/AnaIitico/creditworthiness_classification_model/network/members
[stars-shield]: https://img.shields.io/github/stars/AnaIitico/creditworthiness_classification_model.svg?style=for-the-badge
[stars-url]: https://github.com/AnaIitico/creditworthiness_classification_model/stargazers
[issues-shield]: https://img.shields.io/github/issues/AnaIitico/creditworthiness_classification_model/network/members?style=for-the-badge
[issues-url]: https://github.com/AnaIitico/creditworthiness_classification_model/issues
<!-- [license-shield]: 
[license-url]:  -->
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/josetollinchi/
<!-- [exchange-january-screenshot]: /images/exchange_january_2018.JPG
[exchange-march-screenshot]: /images/exchange_march_2018.JPG -->
