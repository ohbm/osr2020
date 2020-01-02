---
layout: page
title: Projects
project-list:
  - name: rtfMRI
    desc: Real-time fMRI analysis, quality control and visualisation
    url: https://jsheunis.github.io/projects/#rtfmri
    img: /img/rtqc.png
  - name: OpenMR Benelux
    desc: Open science and community building in MRI research
    url: https://jsheunis.github.io/projects/#openmrb
    img: /img/openmrb.png
  - name: Data sharing and GDPR
    desc: New procedures for neuroimage data sharing under the GDPR 
    url: https://jsheunis.github.io/projects/#gdpr
    img: /img/datasharing.png
---

I currently work on multiple projects, some directly related to my Phd, others more broadly to my overall interests. Click on a project below to find out more. If you are interested in learning more or contributing to these projects, feel free to reach out!


{% include list-circles.html items=page.project-list %}

<div id='rtfmri'></div>
<br>
## Real-time fMRI analysis, quality control and visualisation

### Background
Using functional magnetic resonance imaging (fMRI) we can acquire images of the blood oxygenation levels in our brain.
By using a model for how the oxygen concentration in blood vessels in the brain relate to energy consumption due to brain activity, fMRI gives us a proxy measure for actual brain activity that we call the BOLD signal.
In this project we are interested in acquiring, processing, visualising and using this BOLD signal while the patient or study participant is inside the MRI scanner, i.e. in real-time.
Real-time brain activity can be used for different applications, including brain-computer interfaces (BCIs), hyperscanning, and neurofeedback.
Neurofeedback entails showing the person inside the scanner a visual representation of their brain activity, and asking them to regulate this level using the visual feedback.
Our goal is to investigate the use of real-time fMRI neurofeedback in clinical applications. 

### Focus
In preparation for such a clinical trial, however, we first have to ensure the quality of the BOLD signal.
The BOLD signal contains a lot of noise and can be influenced by a number of sources, including participant movement, participant physiology (breathing and heart rate) and scanner artefacts.
It is important that a robust signal processing pipeline is used to remove such noise sources in real-time when possible.
It is also important to visualise and check the quality of the acquired data, both in real-time and after the scanning session.
The focus of this project, and that of my PhD, is to develop new and updated acquisition, processing and quality checking tools to help us improve the quality of the BOLD signal for real-time use.

### Sub-projects

***Real-time fMRI neurofeedback methods - understanding the literature***

How are real-time fMRI neurofeedback researchers processing their participants' BOLD signals? Which methods are they using? Do they report quality checks? Can we investigate this and learn more about what influences the neurofeedback signal and study outcomes?
By reviewing 128 recent fMRI neurofeedback studies, we set out to answer these questions, and more.

You can find the preprint [here](https://doi.org/10.31219/osf.io/xubhq), some code and data [here](https://github.com/jsheunis/quality-and-denoising-in-rtfmri-nf), and interactively explore the summarised studies [here](https://mybinder.org/v2/gh/jsheunis/quality-and-denoising-in-rtfmri-nf/master). 

***Real-time (fMRI) quality control***

Loads of researchers have years and years of experience understanding and correcting quality issues in real-time fMRI data.
Can we collate all of this into a set of best practices? And can we build software tools to make them more accessible to researchers?
Within the fMRI neurofeedback community we are collaborating on such a Matlab-based software tool: rtQC.
The toolbox currently needs beta-testers, so please reach out if you are interested.

Find out more about rtQC on this [poster](https://doi.org/10.5281/zenodo.3239084), and check out the code [here](https://github.com/rtQC-group/rtQC).

***Real-time multi-echo fMRI***

For this project, we are specifically interested in developing multi-echo fMRI acquisition and processing methods for real-time use cases.
Multi-echo denoising methods show promise for conventional resting state fMRI analysis, and our goal is to translate, investigate and describe this for real-time fMRI.

You can find more information on this [poster](https://doi.org/10.5281/zenodo.2553256).

Once my Python skills are up to scratch, I'd also like to contribute more to the [awesome tedana project](https://tedana.readthedocs.io/en/latest/).

*More details to follow!*

---

<div id='openmrb'></div>
<br>
## OpenMR Benelux

### Background
I started OpenMR Benelux as a way to connect with others in the field of MRI research to talk about "open science" and how it is applicable (or not) to our work.
The [first event](https://openmrbenelux.github.io/openmrb2019/) was in January 2019 in Leiden, The Netherlands, on the day before the annual ISMRM Benelux meeting and consisted of talks and discussions.
From the start, I've wanted OpenMR Benelux to be an inclusive community with a low barrier to entry - not too expensive or too elite or too exclusive of anyone.     

### Focus
The goal of the OpenMR Benelux community is to disseminate and promote open research practices within the broad field of MRI.
We want to start discussions and collaborations in an community of students, early/mid career researchers, professors and professionals in the Benelux countries (Belgium, Netherlands and Luxembourg) and beyond.
We do this by organising annual events that elevate collaboration, discussion, teamwork, inclusion, and openness. And we try to make this as fun as possible.
Our next event will be a three day program with talks, discussions, workshops, hackathons and more.

### Relevant details

- Our next event: [OpenMR Benelux 2020](https://openmrbenelux.github.io/page-openmrb-2020/) in Nijmegen, NL. Sadly, registration is closed but we will put all information and content online afterwards. 
- Our website: [https://openmrbenelux.github.io/](https://openmrbenelux.github.io/)

---

<div id='gdpr'></div>
<br>
## Neuroimage data sharing under the GDPR

### Background
Responsible sharing of data and code that underlie the results of a scientific study is an important step towards improving research transparency, fostering inclusivity and building public trust in science.
In health sciences, and neuroimaging research in particular, an important factor when sharing data is privacy of personal or sensitive data.
Ethical review boards at research institutions are responsible for reviewing a study protocol and deciding whether it can continue based on its adherence to the relevant ethical and research integrity principles, which typically include regulations on personal data privacy.
In the European Union, such data privacy requirements are subject to the General Data Protection Regulation (GDPR) as implemented by its member countries.
Despite the increased importance that funders and institutions are starting to place on open science practices, no clear, thorough and openly available guides exist for publicly sharing neuroimaging data under GDPR.

To start ratifying this shortcoming, I suggested a relevant [hackathon topic](https://github.com/ohbm/hackathon2019/issues/47) a the 2019 [OHBM Hackathon](https://ohbm.github.io/hackathon2019/) in Rome.
This started (for me) a fascinating process of discussion and collaboration from which I have gained a lot of insight into privacy and data management, and through which I have met many experts from around the world.  

### Focus
We are a group of international researchers, mostly from EU countries but also from Canada and the USA, who want to make brain research data sharing in accordance with the GDPR an accessible reality. 
We aim to achive this by agreeing on some core relevant GDPR concepts, by creating study planning documentation templates that take these concepts into account, and by creating and sharing this knowledge in accessible ways.

### Sub-projects

***Distilling GDPR concepts for brain data***

The implications of GDPR for (brain) research data sharing are confusing.
It is interpreted and enforced differently in different institutions.
Reaching consensus might be a long shot, but we could first try and work towards a shared language of ideas within the framework of brain data sharing and GDPR.
Our aim here is to identify underlying concepts central to GDPR on which most of us can agree, and to then distill them down to a set of core concepts that have practical implications for our study protocols.

Check out our [working doc](https://docs.google.com/document/d/1Mfbl4DZAw7MRPjSxIiM5sfYU4gX-pcghgj5M1qb84jg/edit).

***Creating standardised templates***

We are creating a set of templates that contain GDPR-compliant wording for ethical review board documentation for studies aiming to share their brain research data.
This builds on great content that already exists in the form of the Open-Brain-Consent initiative.

See the [Github issue](https://github.com/CPernet/open-brain-consent/issues/2) for the main template we are currently focusing on.

***Generating and sharing knowledge***

There's little use in working on these challenging and not sharing our work, especially if the goal is to make such processes and tools more accessible to researchers.
We therefore also want to summarise our project and its outputs and create educational content for general use cases.
We also aim to make this publicly available via a website, and using relatable means of communication like infographics.
We need help, so if this is you please reach out!  


### Relevant details

- Our [Google Drive folder](https://drive.google.com/drive/folders/1zLEUt5Mjq9frucbpMatoBv5w7H37sZNw?usp=sharing) where we share notes
- The OHBM [hackathon project topic](https://github.com/ohbm/hackathon2019/issues/47)
- The [hackathon project update slides](https://docs.google.com/presentation/d/1XEAebPfLFXb2hC2KeQs-mPopUC78Ar4BZ8ZF0h6nhjc/edit#slide=id.p)
- The [Github issue](https://github.com/CPernet/open-brain-consent/issues/2) for the Open Brain Consent template that we are currently focused on
- Our [Mattermost chat channel](https://mattermost.brainhack.org/brainhack/channels/open_brain_gdpr). Join the conversation!   


