# Qualtrics Update: New Survey Taking Experience / Simple Layout

We’ve identified an issue with the new Qualtrics **“Survey Taking Experience / Simple Layout”** option that impacts **M2C2** functionality.

---

## Problem
Enabling the new survey layout deprecates the JavaScript functions **M2C2** uses to get/save embedded data.  
Qualtrics now requires embedded variables to be prefixed with `__js_`.  
This also applies to URL parameters.

---

## Impact
- **M2C2 tasks may not function properly** if the new layout is enabled.  
- This issue only occurs when the new survey experience is turned on.  
- The **legacy survey layout is not affected**.

---

## Workaround
- **Do not enable** the *New Survey Taking Experience / Simple Layout* in Qualtrics.  
- If already enabled, you can **revert to the legacy survey experience**.

---

## Next Steps
We are testing possible fixes to ensure compatibility with both layouts.  
However, since **Qualtrics announced this new layout will become the default for many brands starting June 30, 2025**, this may eventually be unavoidable.

---

## Reference
- [Qualtrics Documentation – Simple Layout](#) *(https://www.qualtrics.com/support/survey-platform/survey-module/look-feel/simple-layout/)*

---

✅ We will update here once a tested solution is available.


# Overview

[`m2c2kit`](https://m2c2-project.github.io/m2c2kit/) is a Typescript/Javascript framework for rapid-creation and iteration of cognitive assessments.

For more information about creating your own m2c2kit tasks, visit our documentation:

https://m2c2-project.github.io/m2c2kit/

## About this Repository

With the web-based implementation of M2C2kit assessments, it is possible for them to be embedded via Qualtrics, REDCAP, and Metricwire (as well as anything else with a WebView).

This repository contains a Qualtrics QSF generator to assist with deployment to Qualtrics.

## Getting Started - Using the Qualtrics QSF Generator

Download and launch qualtrics-qsf-generator.html in your browser. Drag and drop tasks to fit the desired order, input the number of trials for each task and add any additional parameters ('key:value' pairs, comma separated, no spaces). If desired, toggle the checkbox for Qualtrics to auto advance/submit on M2C2 session end, and select your desired language. Finally click the 'Generate Qualtrics QSF File' button, and then click the link to download the QSF file.

1. To import this `.qsf` file onto your Qualtrics instance, follow this guide:

https://www.qualtrics.com/support/survey-platform/survey-module/survey-tools/import-and-export-surveys/#ImportingASurvey

2. Publish your Qualtrics survey and collect data!

⚠️ **Important:** After you have finished testing your generated QSF, we recommend updating the survey flow embedded data variable ```M2C2_DEBUG``` to ```FALSE```

## Participant Management

- You have a couple of avenues for participant management.
  - You can create a List and add the following data columns: ```M2C2_PARTICIPANT_ID```, ```M2C2_SESSION_ID```, ```M2C2_GROUP_ID```, and ```M2C2_WAVE_ID```. Qualtrics will pipe this into your records automatically.
  - You can use the anonymous survey distribution link and append key=value data for the following: ```M2C2_PARTICIPANT_ID```, ```M2C2_SESSION_ID```, ```M2C2_GROUP_ID```, and ```M2C2_WAVE_ID```.

We recommend thoroughly testing your deployment strategy to be sure you have data that is capable of processing.

### Data Access

Using this template would allow you to get started to collect data from m2c2kit assessments via Qualtrics.

To get your data out of our backend, please contact [Dr. Nelson Roque](nur375@psu.edu) for coordination on using our API for data extraction.
