---
type: "project"
date: "2025-06-15" 
# Title of your project (we like creative title)
title: "The Journey of Finding a N400"

# List the names of the collaborators within the [ ]. If alone, simple put your name within []
names: [Mei-Chun Kuo]

# Your project GitHub repository URL
github_repo:  https://github.com/mckuoling/Finding-a-N400-as-a-beginne

# List +- 4 keywords that best describe your project within []. Note that the project summary also involves a number of key words. Those are listed on top of the [github repository](https://github.com/PSY6983-2021/project_template), click `manage topics`.
# Please only lowercase letters
tags: [EEG, mne-python, n400, brainhack]

# Summarize your project in < ~75 words. This description will appear at the top of your page and on the list page with other projects..

summary: "Starting from the raw data, I adapted and translated the original EEGLAB (Matlab) script from ERP CORE into MNE-Python, making all the necessary modifications throughout the preprocessing pipeline to extract the N400."


---
<!-- This is an html comment and this won't appear in the rendered page. You are now editing the "content" area, the core of your description. Everything that you can do in markdown is allowed below. We added a couple of comments to guide your through documenting your progress. -->

## Project definition

### Background

As someone without much programming background and no prior experience with EEG experiments, I took on this project to gain hands-on experience working with raw EEG data — and to learn how to extract ERP components like the N400, which we often see in published studies.
The goal of the project was to use MNE-Python, the EEG analysis tool introduced in our course module. While the module provides a basic demonstration, it only covers some of the core steps. I wanted to understand the full pipeline, from raw data all the way through preprocessing.

### Tools

MNE-Python
[The data preprocessing workflow from NeuralDataScience](https://neuraldatascience.io/7-eeg/introduction.html)

### Data

[ERP CORE: N400](https://erpinfo.org/erp-core)

[EEGLAB (Matlab) working pipline](https://github.com/mckuoling/ERP_CORE/tree/master/N400%20Analysis%20Files/N400/EEG_ERP_Processing)

### Key Changes

Since this project aimed to replicate the N400 results from the ERP CORE dataset, most preprocessing steps and filter parameters followed the original EEGLAB (MATLAB-based) script closely.

One notable adjustment was in the handling of Independent Component Analysis (ICA). As the original authors noted, ICA is a algorithm that the results may vary with each run. In their MATLAB pipeline, the authors documented the specific ICA components that should be removed in order to replicate their original N400 results.

However, since this implementation was done in MNE-Python rather than MATLAB, I adopted an alternative approach based on the [NeuroDataScience tutorial](https://neuraldatascience.io/7-eeg/erp_preprocessing.html#). Specifically, I used the `find_bads_eog()` method to automatically identify and remove EOG-related components. This allows for a more reproducible and automated workflow:

```python
eog_inds, eog_scores = ica.find_bads_eog(raw, threshold=3.0)
print(f"Subject {subject_id} EOG-like ICA components:", eog_inds)
```

## Results

This is the N400 example produced by ERP CORE:
![ERP CORE Example N400](erp_core_n400.png)  
(Kappenman et al, 2021)

And this is the N400 I generated using the same dataset, after adapting the original MATLAB pipeline to MNE-Python.
![My N400 Output](my_n400_result.png)


## Conclusion and acknowledgement

I am very grateful for this course, which allowed me to learn data science in a completely new way. It helped me understand how to learn independently and find solutions. The course also introduced various tools that are commonly used in data science, which is a crucial foundation for beginners.

I also sincerely appreciate the instructors and classmates of this course. Seeing my classmates’ presentations made me realize I’m not alone—facing failures and struggles between different tools and errors is completely normal. I’m also very thankful for the teachers’ continuous encouragement, acknowledging what we have accomplished and pointing out the reasons behind our difficulties. It made me feel very supported and warm.

In this fast-changing era, we can no longer rely solely on teachers to explain everything in class. Making good use of available resources and continuously learning on our own is essential to sustain progress in this field.
