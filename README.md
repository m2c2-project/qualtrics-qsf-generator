# Overview

[`m2c2kit`](https://m2c2-project.github.io/m2c2kit/) is a Typescript/Javascript framework for rapid-creation and iteration of cognitive assessments.

For more information about creating your own m2c2kit tasks, visit our documentation:

https://m2c2-project.github.io/m2c2kit/ 

## About this Repository

With the web-based implementation of M2C2kit assessments, it is possible for them to be embedded via Qualtrics, REDCAP, and Metricwire (as well as anything else with a WebView[cite]).

This repository contains a Qualtrics QSF generator to assist with deployment to Qualtrics.

## Getting Started - Using the Qualtrics QSF Generator

Download and launch qualtrics-qsf-generator.html in your browser. Drag and drop tasks to fit the desired order, input the number of trials for each task and add any additional parameters ('key:value' pairs, comma separated, no spaces). If desired, toggle the checkbox for Qualtrics to auto advance/submit on M2C2 session end, and select your desired language. Finally click the 'Generate Qualtrics QSF File' button, and then click the link to download the QSF file.

1. To import this `.qsf` file onto your Qualtrics instance, follow this guide:

https://www.qualtrics.com/support/survey-platform/survey-module/survey-tools/import-and-export-surveys/#ImportingASurvey

2. Publish your Qualtrics survey and collect data!

### Data Access

Using this template would allow you to get started to collect data from m2c2kit assessments via Qualtrics.

To get your data out of our backend, please contact [Dr. Nelson Roque](nur375@psu.edu) for coordination on using our API for data extraction.
