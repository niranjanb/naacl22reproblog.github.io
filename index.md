---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
--- 
This is the homepage for the [NAACL 2022](https://2022.naacl.org/) Reproducibility Track.

<!-- Output copied to clipboard! -->

<!-----
NEW: Check the "Suppress top comment" option to remove this info from the output.

Conversion time: 0.639 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β31
* Thu Dec 16 2021 06:57:03 GMT-0800 (PST)
* Source doc: Reproducibility Track NAACL 2022
----->



# Reproducibility Track NAACL 2022

This track introduces a badge system to incentivize authors of NAACL papers to release models, code, and other information necessary to reproduce the main results/findings of their papers. After notification of acceptance and before the camera ready is due authors will have the option to earn up to three reproducibility “badges” by 1) providing a link to code, 2) providing a link to a trained model, and 3) participating in a verification process where a trained model will replicate some result from the paper. This document outlines the details of this track.

# Contents


 - [Why is NAACL running this track?](#why-is-naacl-running-this-track) 
 - [What is the benefit to authors?](#what-is-the-benefit-to-authors) 
 - [What are these badges and how do you earn them?](#what-are-these-badges-and-how-do-you-earn-them)
 - [What resources and support are available?](#what-resources-and-support-are-available)
 - [Other FAQ](#faq)

## Why is NAACL running this track?

As NLP matures as a scientific discipline our progress rests on the reproducibility of our scientific claims. While reproducibility has risen to the forefront of many disciplines, NLP has a distinct advantage: our research produces scientific artifacts such as code and trained models that we can share. Doing so facilitates comparisons against previous work, and gives starting implementations for new research to build on. In addition, as the computational cost of our experiments has increased in recent years, releasing trained models saves us from having to rerun experiments others have already run.

## What is the benefit to authors?

NAACL will highlight the papers that successfully participated in the track by (i) assigning badges to these papers in  the conference proceedings, (ii) highlighting them in the various material produced as part of the conference  (e.g. a separate page listing papers with badges), and (iii) issue best reproducibility track paper awards.

These can act as a starting point for future researchers who are looking to start a project, and authors will get broader adoption of their work. 

## What are these badges and how do you earn them?

The papers accepted to the NAACL conference can apply for three types of badges.

**Open-Source Code Badge**: Authors submit a link to code. The code itself will not be run by reviewers (though it may be visually checked), so it is up to the authors to provide appropriate documentation. If authors participate in Badge 3, we recommend authors include the dockerfile in their repository. PapersWithCode has a code completeness checklist [here](https://medium.com/paperswithcode/ml-code-completeness-checklist-e9127b168501).

**Trained Model Badge**: Authors submit a link to download a trained model. Similar to Badge 1, the model will not be run by reviewers (though other aspects may be checked, like the size on disk just to confirm the link works).

**Reproducible Results Badge**: Authors verify that their model replicates a result they specify from their paper. This is meant to be similar to a unit test, where the output of a model the authors submit is matched against a string they submit (which represents the result from their paper the authors wish to have replicated). 

To do this, authors will choose a model (typically one they trained) and package it into an executable docker container using [THESE INSTRUCTIONS]. They will choose the main result from their paper that they wish to have replicated and format it as a string (e.g., “Accuracy on TASK_X: 85%”). They will submit the executable docker container and the string, and the server will execute it and verify that the output of the execution exactly matches the string.

We have partnered with the Allen Institute for AI, who will donate the computational resources necessary. We can articulate from the perspective of the paper what earning this badge means.

The primary goals of these three badges is to formalize how authors can release code and trained models, and to make it easier for other researchers to find and use them. These badges build on the suggested [badges](https://www.acm.org/publications/policies/artifact-review-badging) from the ACM. The first two badges are types of “Artifact Available” badges which indicate that authors make some (unverified) materials available, and the third is a “Results Replicated” badge also meant to provide a working runtime environment so future researchers can easily build on or compare against the published work. 

### Badging Process and Timeline

The badging process will involve the following steps:

#### 1. **ADD DATE** Signing up for badging 

#### 2. ** ADD DATE ** Submission Window

#### 3. ** ADD DATE ** Notification

#### 4. ** ADD DATE ** Post Acceptance Options



#### How to apply

TO ADD: How a reader of this doc will interface with this process. They will get an email on the date of the acceptance notification which will include a link to a form. That form will have three fields: 1) a text box in which they can enter a link to their code, 2) a text box in which they can enter a link to download their trained model, 3) a check box to indicate if they want to participate in the verification process.

<!-- ### Timeline  #### Submission Window #### Date of Notification -->


#### How are the submissions evaluated?**

The experiments will be run on an [a2-high gpu-1g](https://cloud.google.com/blog/products/compute/a2-vms-with-nvidia-a100-gpus-are-ga?authuser=1) VM on Google Cloud, which has an A100 GPU with 40 GB of GPU memory, and 85 GB of RAM, with X space on disk (maybe up to 1 TB).

We will accept Docker images up to 50 GB in size. These instances will be connected to the internet, so if a dataset is too large to fit in the image, authors can have their image download it when run. We can provide cloud credits to allow users to try running their system on the correct type of cloud instance. Authors can fill out a Google form with their paper ID, and . 

We should be explicit about the datasets that people upload -- authors should of course not 

We will only retain the submitted Docker images for X number of days, and it will not be made public. It will be automatically deleted after [DATE].

The intent is for this to evaluate inference of trained models, not to train models from scratch. 

## What resources and support are available?

	Instructions and How-To documents for dockerization and submission

	Office hours?

	Docker Registry

	GCP credits 


### How are the data and code protected?

[Here we will discuss licensing, and privacy policy. We should not be held liable for the decisions they make. For example, if their data comes with a license that states it should not be given to third parties, and they give it to us, they are the ones at fault.]

### Recommendations on how to release code 

Some instructions for how to release a useful code repository can be found here: https://github.com/paperswithcode/releasing-research-code

### Anonymization and Review Process

[TBD]

## FAQ

Q: Does this disadvantage papers that can’t achieve these badges? 

A: No. These badges should only be considered for a subset of all papers presented at NAACL; there are many types of papers for which it’s not appropriate to submit, for example, an executable model. Papers which introduce a dataset, papers which primarily focus on linguistic or mathematical theory, papers from industry labs that can’t publicly release scientific artifacts, and position papers are all types of papers that we value as a community that likely won’t be covered by these badges.

Q: My model is larger than the maximum size for the docker container! Or, my model was implemented on other hardware that’s not supported by the cloud instance available! Can I still earn Badge 3?

A: Yes, by hosting and executing your model on your own, and providing API access which you query from the docker container.

Q: Do I need to earn Badge 1 to get Badge 2, or Badge 2 to get Badge 3?

A: No, authors can earn any subset of the three badges.

Q: What if I can’t publicly release my model or data, but still want to earn Badge 3 (showing my results are reproducible)?

A: That’s great. Everything submitted for Badge 3 will be deleted after verification, and will not be made public.

Q: Do I need to anonymize the code, model, or executable? 

A: No. This process will take place after notification of acceptance, so it will not interact with double-blind reviewing of the paper. In addition, much of this process will be automatic, and badge reviewers will only check to confirm that, for example, the links authors provide work as intended, and that there aren’t errors in the automatic verification process.

Q: I don’t have root access on my machine to create the docker image required.

A: 

Q: I’m stuck creating a docker image. Can you help? 

A: Yes, we will have an “office hours” where volunteers will help debug on [INSERT_DATE]

Q: What criteria willHow will the "Most Reproducible" 

Outline our incentive structures for participation:



## TO BE DELETED
* Ideas we’ve settled on:
    * The badges will be presented in the proceedings
    * The papers that earn each badge will be presented in a list on the conference website
* Ideas we’re discussing:
    * Perhaps we should award GCP credits for people to prototype
    * We might have a “most reproducible” paper award
    * Top participants could be invited to give a talk in our “track”
    * Social media chairs could tweet about the work

We can have a few students go through the process, specifically a good amount of women, to see how we can improve the process. This allows us to get quotes from people that we can include on the website.
