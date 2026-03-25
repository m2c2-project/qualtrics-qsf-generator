# Qualtrics Compatibility Update

As of version **2026_03_25**, the Qualtrics QSF Generator is compatible with both the **new Survey Taking Experience / Simple Layout** and the **legacy survey layout**.


# Overview

[`m2c2kit`](https://m2c2-project.github.io/m2c2kit/) is a TypeScript/JavaScript framework for the rapid creation and iteration of cognitive assessments.

For more information about creating your own m2c2kit tasks, visit our documentation:

https://m2c2-project.github.io/m2c2kit/

## About this Repository

With the web-based implementation of M2C2kit assessments, they can be embedded in Qualtrics, REDCap, and MetricWire, as well as in other platforms that support a WebView.

This repository contains a Qualtrics QSF Generator to assist with deployment to Qualtrics.

## Getting Started - Using the Qualtrics QSF Generator

Download and open `qualtrics-qsf-generator.html` in your browser. Drag and drop tasks into the desired order, enter the number of trials for each task, and add any additional parameters (`key:value` pairs, comma-separated, with no spaces). If desired, enable the checkbox for Qualtrics to auto-advance/submit when the M2C2 session ends, then select your desired language. Finally, click **Generate Qualtrics QSF File** and use the download link to save the QSF file.

1. To import this `.qsf` file onto your Qualtrics instance, follow this guide:

https://www.qualtrics.com/support/survey-platform/survey-module/survey-tools/import-and-export-surveys/#ImportingASurvey

2. Publish your Qualtrics survey and collect data!

⚠️ **Important:** After you have finished testing your generated QSF, we recommend updating the Survey Flow embedded data variable `M2C2_DEBUG` to `FALSE`.

## Participant Management

- You have a couple of options for participant management.
  - You can create a contact list and add the following data columns: `M2C2_PARTICIPANT_ID`, `M2C2_SESSION_ID`, `M2C2_GROUP_ID`, and `M2C2_WAVE_ID`. Qualtrics will pipe these values into your records automatically.
  - You can use the anonymous survey distribution link and append `key=value` parameters for `M2C2_PARTICIPANT_ID`, `M2C2_SESSION_ID`, `M2C2_GROUP_ID`, and `M2C2_WAVE_ID`.

We recommend thoroughly testing your deployment strategy to ensure the resulting data can be processed correctly.

### Data Access

This template will help you get started collecting data from m2c2kit assessments through Qualtrics.

To get your data out of our backend, please contact [Dr. Nelson Roque](nur375@psu.edu) for coordination on using our API for data extraction.
