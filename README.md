# <p align=center> This repository supplements the Survey [Relevance of Explainable AI in Computer-Aided Brain Tumor Diagnosis - A Survey](https://arxiv.org/abs/2201.09873)
[Fahad Shamshad](https://scholar.google.com.pk/citations?user=d7QL4wkAAAAJ&hl=en), [Salman Khan](https://salman-h-khan.github.io/), [Syed Waqas Zamir](https://scholar.google.es/citations?user=WNGPkVQAAAAJ&hl=en), [Muhammad Haris Khan](https://scholar.google.com/citations?user=ZgERfFwAAAAJ&hl=en), [Munawar Hayat](https://scholar.google.com/citations?user=Mx8MbWYAAAAJ&hl=en), [Fahad Shahbaz Khan](https://scholar.google.es/citations?user=zvaeYnUAAAAJ&hl=en), and [Huazhu Fu](https://hzfu.github.io/)
</p>

Brain tumors are considered a severe disease, in which time misuse or fortuitous errors can put a person’s life in jeopardy. Diagnostic skills of brain
anomalies vary depending on their experience of the doctor; however, there
is consensus about the immense importance of Magnetic Resonance Imaging
in the diagnostic process.
To support the diagnosis process, Computer Aided Detection (CADx)
is implemented. CADx processes digital information to be able to obtain
further details of a disease, as well as, simulate the deductive inference process
of professionals to support their final decision. However, CADx systems’
output rarely constitute fully-understandable nor reliable tools, which in turn
means there is room for researching CADx
Recent literature suggests that Explainable Artificial Intelligence (XAI) is
a widely acknowledged research field that holds substantial promise for the
more accountable artificial intelligence-based systems. XAI will and does
play a crucial role in medical applications, nonetheless, the answer to how
novel studies tackle the trade-off between accuracy and explainability fails
to be fully explored and could be further scrutinized. Similarly, achieving
consensus on explainable evaluation metrics is still in infacy.
This survey aims to bridge the gap between CADx and XAI by making an
exhaustive literature review and comparison among state-of-the-art methodologies for Brain Tumor Detection based on Magnetic Resonance Imaging.
Also, this review features an analysis of the common metrics and key performance indicators considered for a respectable explainable evaluation.

## Introduction
Cancer is considered the second leading cause of death after cardiovas-
cular diseases [1]. According to the American Cancer Society (ACS) cancer
is considered one of leading public health problems across the world. The
ACS statistics of new cases of cancer across the United States lead to the
interpretation that this illness should be considered of great relevance as it
compromises the well being of a compelling group of people. In spite of the
decline in cancer rates since the 1990s, the number of cases is still significant
[2]. It must be emphasized that out of all types of cancer, brain cancer has
the lowest survival rate [3]. Malignant brain tumors account for a dispropor-
tionate burden of cancer mortality because of their low survival rate; only
one-third of individuals will endure at least 5 years after diagnosis [4].
As for today, in clinical practice, doctors and medical practitioners have
to manually identify a tumor’s existence for the prescription of subsequent
medical treatments.
An early cancer detection is required for increasing full recovery chances
[5]. Despite the passing of time, there is still a significant percentage of mis-
diagnosis in medical imaging. For instance, an analysis of the Comparative
Benchmarking System (CBS) of the insurance program (CRICO) [6] reviewed
in depth 29,777 cases of medical malpractice. 1325 cases named radiology as
the primary responsible service, of which 42% turned out to be high severity
cases. Thia release that the task of classifying tumor images can be seen
as trivial from a merely computer vision approach. Medically speaking, im-
ages are too diverse and require high expertise to be accurately interpreted.
There is a remarkable need of developing efficient, transparent, non-prone to
error tools in the medicine. Strides in Machine Learning (ML) have led to an
emerging trend of developing Artificial Intelligence (AI) systems in diverse
range of fields. ML is powering several medical applications and there is a
significant interest on using Deep Learning (DL) along with Neural Networks
(NNs) due to their advantages while recognizing images [7]. CADx systems
can improve clinical performance by reducing not only misclassifications, but
also misinterpretation of images that may lead to incorrect prescriptions of
certain treatments. Outputs of assisted diagnosis can be used as “second opinions”, to advocate for final diagnosis. CADx is an established concept
that has equal participation of doctors and computers [8].
Along with the AI developing field, the necessity for explanations backing
up the model’s results have also emerged. When a significant medical decision
must be made, an AI that suggests a course of action with reasonable evidence
and transparency, rather than simply define one is desired [9]. Explainable
models estimate the influence of all features on the model predictions [10],
granting tools and methods for a better understanding and interpretation of
deep learning outcomes. An explanation is any information that can help
the user understand and communicate to others why the model exhibits a
particular decision-making pattern [9] [11]. For medical AI applications as
CADx to be accepted and included in clinical practices, Explainable Artificial
Intelligence (XAI) is determining.
However, a thorough analysis of novel approaches and methodologies of
CADx including XAI have highlighted the lack of established XAI evalua-
tion, as a result of the nonexistent consensus in key performance indicators of
inteterpretability, implying the need of an urgent definition of explanability
metrics. According to [12], only 5% of the studied papers until 2018 by this
survey focused on assessing interpretability methods. Furthermore, there is
an evident scarcity in studies contemplating a proper XAI evaluation in col-
laboration with professionals in the field [13]. Out of 22 studies from 2019 to
2022, only three approaches [14] [15] [16] evaluated the model effectiveness
with professionals. Despite the development of some general-purpose ex-
plainable approaches, interpretability is a domain-specific concept [17] [18],
meaning that there cannot be an all-purpose solution [19]. It is imperative
to take into account the application domain and use case for each problem,
that is to say, Brain Tumor Diagnosis. This survey will further develop the
stated gaps and showcase opportunities as well as future research needs.
This paper is arranged as follows. Section II explains the used strategy
followed to successfully scrutinize the state-of-the-art research and develop
the survey. Section III provides some detailed background explaining con-
cepts and the basis of neuroscience with some medical insight. Section IV
discussed image recognition and its application prospects in medical imaging.
Section V explains CADx and showcases projects in the field, while section
VI focuses on CADx focused in brain tumors. Section VII describes XAI
and its characteristics and section VIII develops on CADx focused on brain
tumors with XAI. Section IX and X highlight important aspects about the
reviewed approaches. Section X discloses the importance of XAI evaluation Finally section XI and XII presents a final discussion and conclusions.

## Research Strategies
The methodology and systematic approach was performed under the fol-
lowing criteria: First, the main ideas and concepts were analysed in an initial
and superficial overview. Then a scoping review was performed to be famil-
iarized with the topic. Second a deeper research took place to find significant
information (information retrieval) and milestones in the development of the
state of the art. In this phase a protocol was constructed for critically eval-
uating the relevance of the found articles and books. Third, the found body
of knowledge was analyzed, critical hypothesis were made based of results
and conclusions, to finally make an exploration of assumptions, limitations
and areas of uncertainty.
The review included all articles that were relevant, directly linked to the
keywords, and current, no earlier than 2018, and were published in high
known journals or databases. The main keywords for the literature search
were: Explainable Artificial Intelligence (XAI), Machine Learning (ML), In-
terpretability, Computer Aided Diagnosis (CADx), Diagnostics, Magnetic
Resonance Imaging (MRI) and Brain Tumor. Additionally, the vast major-
ity of the research papers cited in this survey were found in: Scopus, IEEE
Xplore, PubMed, Google Scholar, ResearchGate, ScienceDirect and ACM
digital library. The search strings used in this survey included, but are not
limited to:

• TITLE-ABS-KEY( (Explainable Artificial Intelligence) OR XAI OR (Explainable AI) OR Diagnostics). 

• TITLE-ABS-KEY( (High Computation) OR (Brain Tumor) OR (Explainable AI)).

• TITLE-ABS-KEY( (Medical Imaging) OR MRI OR (Brain Tumor)).

• TITLE-ABS-KEY( (Brain tumor) OR MRI OR (Explainability)).

• TITLE-ABS-KEY( (Magnetic Resonance Imaging) OR (Deep Learning) OR (Brain Tissues)).

Articles that described methods for diagnosis in different context than AI,
articles that described the philosophy of explanation, duplicated or repub-
lished articles, articles published in workshops and technical reports, were all
excluded.

## Background
Physicians will follow a series of steps to understand a magnetic resonance image [20]. First step is to identify the scan, the imaging sequence, and the slice. Then they will look for asymmetry. Next, they will need to identify the lesion causing the asymmetry, and its density/intensity, decide if contrast enhancement pattern may be useful, and locate the lesion in the extra-axial compartments (outside the brain), or intra-axial compartment (in the brain parenchyma). This methodology carries out a lot of responsibility. Moreover, the per- son carrying out this decision has to have gone through an extensive prepa- ration journey to be specialized in diagnosing and treating diseases of the Central Nervous System (CNS). Neuroradiologists are Graduates of medical school, that completed a four years long residency in radiology, concluded four months of mandatory training in radiology, were then eligible for the ra- diology board certification and completed a fellowship of two additional years of specialized training [21]. On average neuroradiologist have more than 10 years of training after their undergraduate education. The role of radiology in diagnostic error [22] states that the process of medical diagnosis involves a compound network of interactions between the patient and the healthcare system. Being a dynamic process in need of multiple interaction cycles with the patients, failure can arise at any given stage, which may result in late or inaccurate diagnosis, as well as inappropriate treatment. Cancer can be the source of almost any symptom but once neurooncol- ogy clinicians have enough evidence to suspect a patient might have cancer [23], they will ask about the family medical history and perform a physical exam. Then, doctors will run a series of diagnostic tests, including lab tests, endoscopy, biopsy and imaging tests. Imaging can be useful for reasonable differentials. The central nervous system (CNS) also known as neuraxis, consists of the brain (encephalon) and the spinal cord (medulla spinalis). The CNS connects information from the entire body and coordinates activity across the whole organism [24]. Any type of brain tumor can cause considerable problems as the rigidity of the skull leaves no room for the tumor to expand [25]; for example, if tumors expand to parts of the brain that control vital functions, some derived problems include feeling of weakness, complications in walking, trouble with balance, partial or complete loss of vision, difficulty understanding or using language, and complications related to memory. Al- though the etiology remains relatively unexplored, the classification of brain tumors has progressed in parallel with expanding molecular understanding and advances in detection and diagnosis. Thus, brain tumors can be classi- fied into two main categories, Malignant (cancerous, 29.7% of tumors) and Non-Malignant (benign or noncancerous, 70.3% of tumors) [26], statistical distribution found in Fig. 1. Malignant and nonmalignant brain and other CNS tumors constitute a numerous assemble of over one hundred histologi- cally specific sub-types with distinct epidemiology and clinical characteristics according to the 2021 WHO Classification of Tumors of the Central Nervous System [27].

![ Figure 1: Distribution of Brain Tumors, classified as the two major categories. Data obtained from [28]. ](image-url)

All forms of cancer are revealed to involve dynamic modifications in the genome which means that they arise from alterations of critical cellular func- tions such as apoptosis, proliferation, and tissue invasion [29]. In fully devel- oped brains, neural stem cells and progenitor cells (glia) commonly possess features associated with cancer of the CNS, including a robust proliferative potential and a diversity of progeny [30]. Actions among molecules in a cell that lead to certain product (cellular pathways) that operate in many brain tumors, do also regulate neural stem cells [31]. Further analysis suggest that stem and progenitor cells in the CNS are at major risk of tumorigen- esis. Malignant gliomas are the most common primary brain tumors, and glioblastomas are among the deadliest of human cancers. Despite being rec- ognized and treated since the middle 19th century, nowadays improvement in its survivability has not increased substantially. The predominant histologic subtype for malignant tumors are glioblastomas. In Table 1, tumors of the CNS and their associated cell types are described, glioblastomas originate in glial astrocyte cells, this type of tumor accounts for nearly half, 48.6%, of all malignant tumors in all ages combined, as seen in Fig. 2. According to the World Health Organization (WHO) [32], malignant brain tumors are classified into grades I to IV and glioblastomas are classified as a grade IV tumor.

![ Figure 2: Classification of malignant brain tumors and their incidence rate. Data obtained from [28] ](image-url)

## Medical Image and Computer Vision

Medical imaging is defined as a technique that produces images of hu- man organs that help identify and treat diseases by making nondestructive scanning of a certain soft tissue. Magnetic Resonance Imaging or MRI is a medical imaging procedure that is non-invasive and does not inflict any pain. This modality has evolved from being a method with a bleak future to be one of the most used in medicine. MRI was introduced in the 70s and has become nowadays the imaging method of choice for a large proportion of radiological examinations [33], It is considered to be one of the most accurate techniques for cancer detection and classification of images on the brain tissue, as it gives rich data for clinical analysis and biomedical research [34]. As described by McRobbie et al. [33], the reason MRI is vastly used is that allows the user to produce images with a wide range of contrasts by using different imaging techniques (known as pulse sequences) and by controlling the timing of the sequences. This makes it possible to make the tumour dark and brain tissue brighter. All MR images are produced using a pulse sequence, which is then stored in the scanner computer. The sequence contains radiofrequency (RF) pulses and gradient pulses which have carefully controlled duration and timings. The gradient pulses make the characteristic ‘knocking’ noise when the image is acquiring a scan. Many different types of sequences can be performed, but they all have timing values called Repetition Time (TR), and Time to Echo (TE), which can be customized. TR and TE are set in order to get the required image contrast. MRI uses the natural properties of hydrogen which, as part of water or lipids, makes up 75–80% of the human body. The most important properties are the proton density (PD), and two characteristic times called spin-lattice relaxation time and spin-spin relaxation time, denoted T1 and T2, respectively.

