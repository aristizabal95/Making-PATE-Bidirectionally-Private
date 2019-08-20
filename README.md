# Making-PATE-Bidirecitonally-Private
A step-by-step guide demonstrating how the PATE Framework works and how to make it bidirectionally private by adding an encryption layer.

PATE, or Private Aggregation of Teacher Ensembles, is a machine learning framework proposed by Papernot et al. in the paper [Semi-Supervised Knowledge Transfer for Deep Learning from Private Training Data](https://arxiv.org/pdf/1610.05755.pdf). This framework allows for semi-supervised learning with private data while retaining both intuitive and strong privacy guarantees.

PATE has shown to achieve state-of-the-art privacy/utility trade-offs, while also having a flexible and widely applicable implementation. There are, however, some situations in which this framework struggles. This is when there is no access to public data, or when the student’s data is necessarily private. PATE requires the student to share its data with all the teachers, and therefore no privacy is guaranteed in this process. An example of such a situation is when a Hospital wants to train a neural network for diagnosis and uses other hospitals as “teachers” to label its dataset. In such a situation, PATE may be infeasible, because the “student” hospital is probably obliged (either morally or legally) to maintain its dataset private.

Because of this, an additional step is proposed, where the teacher ensemble is considered as “Machine Learning as a Service” (MLaaS), and encryption is added to provide secrecy for the student’s dataset. This new implementation opens up the possibility to use PATE in scenarios were none of the parties have an interest of sharing their data. Be it for legal reasons, as the example provided above, or for market reasons, like tech companies working together to develop better applications without ever needing to expose their client's usage data.

Here, we are going to explore how to apply these changes and how it affects the PATE Framework procedure.

# Contents
This repo contains a notebook with a step-by-step guide on implementing PATE and adding encryption. Since this is for educational purposes, the MNIST dataset was used to demonstrate the procedure and the issues at hand.

# Additional links
A Medium Article has been published, where this project is fully explained and demonstrated with visuals and commented code. It is higly recommended to read this article along with this project.

[Making PATE Bidirectionally Private. Alejandro Aristizábal Medina](https://medium.com/@alejandro.aristizabal24/making-pate-bidirectionally-private-6d060f039227)

# Additional Notes
This repo was developed  as part of Udacity’s Secure and Private AI Nanodegree Program. The intention of this repo is to present and explain my final project for the course and it should be regarded as such.
