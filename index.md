---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
--- 
<!-- This is the homepage for the [NAACL 2022](https://2022.naacl.org/) Reproducibility Track.-->

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

This track introduces **a badge system** to formalize expectations around reproducibility of our commmunity's research findings. The main idea is to incentivize authors of [NAACL 2022](https://2022.naacl.org/) papers to release models, code, and other information necessary to reproduce the main results/findings of their papers. This document outlines the details of this track.

**TLDR;** After notification of acceptance and before the camera ready is due authors will have the option to earn up to three reproducibility “badges” by 1) providing a link to code, 2) providing a link to a trained model, and 3) participating in a verification process where a trained model will replicate some result from the paper. 

See our **2 minute** [video]() for a quick introduction. 


## Important Dates
- ** Submission Window ** --
- ** Badging Acceptance Notification ** -- 


# Outline

- [Why do we need this track?](#why-do-we-need-this-track) 
- [What is the benefit to authors?](#what-is-the-benefit-to-authors) 
- [What are these reproducibility badges?](#what-are-these-reproducibility-badges)
- [What is the process and timeline for participating?](#what-is-the-process-and-timeline-for-participating)
- [What resources and support are available?](#what-resources-and-support-are-available)
- [What restrictions and considerations apply to the submitted systems?](#what-restrictions-and-considerations-apply-to-the-submitted-systems)
- [Other FAQ](#faq)
- [Committee](#committee)

## Why do we need this track?

Our progress as a scientific discipline rests on the reproducibility of our scientific claims. Sharing code and trained models facilitates comparisons against previous work, and gives starting implementations for new research to build on. Furthermore, 
with the rapid rise in computational cost of our experiments, releasing trained models saves costs of rerunning experiments others have already run. This track is aimed at (a) incentivizing authors to facilitate reproducibility, and (ii) introducing some formalization of the process and our expectations for reproducible research as a community.


## What is the benefit to authors?

The main benefit to authors is in making their work reproducible in a way that will enable broader adoption of their work. In addition, NAACL will highlight the papers that successfully participated in the track via the following:

- **Badges:** Assigning badges to these papers in  the conference proceedings
- **Spotlight Badged Papers:** NAACL will highlight badged papers in various material produced as part of the conference  (e.g. a separate page listing papers with badges).
- **Best Reproducibility Track Paper Awards:** issue best reproducibility track paper awards.

## What are these reproducibility badges?

The papers accepted to the NAACL conference can apply for three types of badges.

**1) Open-Source Code Badge**: Authors submit a link to code. The code itself will not be run by reviewers (though it may be visually checked), so it is up to the authors to provide appropriate documentation. If authors participate in Badge 3, we recommend authors include the dockerfile in their repository. PapersWithCode has a code completeness checklist [here](https://medium.com/paperswithcode/ml-code-completeness-checklist-e9127b168501).

**2) Trained Model Badge**: Authors submit a link to download a trained model. Similar to Badge 1, the model will not be run by reviewers, though other aspects (e.g. size on disk) will be checked to confirm that the provided link works.

**3) Reproducible Results Badge**: Authors verify that their model replicates a result they specify from their paper. They will package their model (typically one that has already been trained) along with a replication test script into a Docker container using our [instructions]() and upload it to **WHERE???**. The server will execute the test script in the container and verify that its output matches the key result that the authors provide at the time of submission.


In addition to detailed guidelines and materials, the track will also provide [compute resources, a discussion forum, and office hours](#what-resources-and-support-are-available) to facilitate this. Thanks to our sponsors [Allen Institute for AI](https://allenai.org/) and [Google](https://www.google.com/) for providing resources.


The primary goals of these three badges is to formalize how authors release code and trained models, and to make it easier for other researchers to find and use them. These badges build on the suggested [badges](https://www.acm.org/publications/policies/artifact-review-badging) from the ACM. The first two badges are types of “Artifact Available” badges which indicate that authors make some (unverified) materials available, and the third is a “Results Replicated” badge also meant to provide a working runtime environment so future researchers can easily build on or compare against the published work. 

## What is the process and timeline for participating? (Group)

The badging process will involve the following steps:

### 1. Request for participating in track (ADD DATE)

The NAACL paper acceptance notification emails will contain a link to a form through which authors can apply for the reproducibility badges.

### 2. Dockerization Support and Office Hours (ADD DATE)

Through out the submission window, we will host a email discussion form and hold **weekly???** office hours to help with the dockerization. 

Further, to assist with development we will provide Google Cloud Platorm credits. See the [resources](what-resources-and-support-are-available) section for more details.

### 3. Submission (ADD DATE)

The authors can submit anytime from the receipt of their paper acceptance notification until the track submission deadline **To Be Announced**

The track submission form will have three fields: 1) a text box in which they can enter a link to their code, 2) a text box in which they can enter a link to download their trained model, 3) a check box to indicate if they want to participate in the verification process.


### 4. Evaluation and Notifications (ADD DATE)

Each submission will be evaluated by **[XXX]** reviewers. 

Systems submitted for the Reproducibility Results Badge will be run on an high-end machine. For example, a [a2-high gpu-1g](https://cloud.google.com/blog/products/compute/a2-vms-with-nvidia-a100-gpus-are-ga?authuser=1) VM on Google Cloud, which has an A100 GPU with 40 GB of GPU memory, and 85 GB of RAM, with X space on disk (maybe up to 1 TB). Exact details on the requirements will published .

From those that qualify for the badges, we will select three to be recognized as the **Best Reproducibility Track Papers**. This evaluation will focus on the reproduciibility aspects of the paper. See [best paper awards section] for more details.

All badging notifications will be sent to the authors via email by **ADD DATE**.

## What resources and support are available?

	Instructions and How-To documents for dockerization and submission (Daniel)

	Office hours? (Daniel and Yash)

	Docker Registry (Pete?)

	GCP credits (Annie)


## What restrictions and considerations apply to the submitted systems? (Jesse and Pete)

### Hardware Requirements

We will accept Docker images up to 50 GB in size. These instances will be connected to the internet, so if a dataset is too large to fit in the image, authors can have their image download it when run. 

Note the intent here is to evaluate inference of trained models, not to train models from scratch. 


### License and IP Protected Data and Code

[Here we will discuss licensing, and privacy policy. We should not be held liable for the decisions they make. For example, if their data comes with a license that states it should not be given to third parties, and they give it to us, they are the ones at fault.]


### Code and Data Retention beyond the NAACL timeframe.

We will only retain the submitted Docker images for X number of days, and it will not be made public. It will be automatically deleted after [DATE].


## FAQ (Group)

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


## Committee
1. Daniel Deutsch, UPenn
2. Yash Lal, Stony Brook University
3. Annie Louis, Google
3. Pete Walsh, Allen Institute for Artificial Intelligence
4. Jesse Dodge, Allen Institute for Artificial Intelligence
6. Niranjan Balasubramanian, Stony Brook University

