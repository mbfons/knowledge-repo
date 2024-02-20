## Privacy Enhancing Technologies

### Definition

Privacy Enhancing Technologies (PETs) are a set of technologies and methods that allow the collection, processing, analysis and dissemination of insights, often in a collaborative way, while protecting the confidentiality of data (often personal).

PETs can play a key role not only regarding privacy but more broadly in data governance.

There is no universally accepted definition, but below some definitions from relevant bodies are highlighted:

>  “PETs are technologies that embody fundamental data protection principles by minimising personal data use, maximising data security and/or empowering individuals.” - ICO of the UK (2022)

> "privacy-preserving data sharing and analytics technologies, which describes the set of techniques and approaches that enable data sharing and analysis among participating parties while maintaining disassociability and confidentiality. Such technologies include, but are not limited to, secure multiparty
computation, homomorphic encryption, zero-knowledge proofs, federated learning, secure enclaves, differential privacy, and synthetic data generation tools." - White House, 2022

> "Software and hardware solutions, ie systems encompassing technical processes, methods or knowledge to achieve specific privacy or data protection functionality or to protect against risks of privacy of an individual or a group of natural persons." - European Union Agency for Cybersecurity (ENISA)


### State of Play

PETs are not necessarily new, but advances in computing power and infrastructure have led to new possibilities in their use for data processing and sharing.
Many of these developments are still novel or emerging. Namely, policy makers, regulatory bodies and authorities are starting to consider how to incorporate PETs in and their role underpinning new paradigms of data protection by default and by design.

They are seen to be able to increase both the data utility and data protection, as opposed to traditional trade-offs between utility and protection.

### Categorisation

Similar to definition, there is no universally acknowledged and stable categorisation and taxonomy of PETs. Rather, different organisations have developed distinct categorisations over time.

Namely, PETs could be divided into the following four categories (OECD):
* **Data obfuscation tools**: tools that increase levels of privacy protection by changing the data, by adding "noise" or by suppressing disclosive information:
  
    * Types: e.g. anonymisation and pseudonymisation tools; synthetic data; differential privacy, zero-knowledge proofs (ZKP);
    * Advantages:
    * Cautions: needs correct implementation; data not necessarily anonymous since some tools or added data may be able to reidentify 

* **Encrypted data processing tools**: tools that allow data to remain encrypted during use (data remains unmodified but hidden).

    * Types: e.g. homomorphic encryption; multi-party computation; trusted research environments / secure data environments
    * Advantages: data does not need to be decrypted before use
    * Cautions: computation and infrastructure costs, data quality ...

* **Federated and distributed analytics**: tools or procedures that allow analytical actions to be run on data, but where the data is not visible or accessible while executing those actions.

    * Types: e.g. federated learning protocols
    * Advantages: microdata does not need to be shared by parties to allow for insights; scalability
    * Cautions: computation and infrastructure costs, connectivity, information on data models and interoperability
 
* **Data accountability tools**: tools that seek to enhance data protection and privacy by allowing for data subjects to have oversight, agency and control over their own data. Not strictly a PET since their primary aim is not data confidentiality itself from a technical standpoint but rather control and accountability. 

    * Types: e.g. personal data stores, accountable systems
    * Advantages: user control and transparency
    * Cautions: low maturity and technology readiness of tools; narrow scope use cases; few standalone applications; not strictly a PET

PETs tend to not be standalone tools, but rather used together with other PETs or other organisational tools to achieve data governance objectives.

### Tools

#### Data obfuscation

##### Anonymisation

Anonymisation is the process of removing from the data the identifying elements, such that re-identification of a data subject is not possible.
Anonymised data should not be linkable or traceable back to an individual, even through enrichment.
True anonymisation can however be hard to achieve.
The concept of anonymisation is widely used in legislation, namely in GDPR.

##### Pseudonymisation

Pseudonymisation is a deidentification process that involves removing potentially identifiable information about data subjects from the data, in order to reduce reidentification risk.
Pseudonymisation can be reversed typically. It preserves the ability to, if need arises, combine the information with other identifiable datasets, either through a common key or encryption process.
It is a weaker form of deidentification than anonymisation.

##### Synthetic data

Synthetic data is generated rather than real source data. It is often generated from population models. Often it is desired that artifical data has similar statistical properties to the source data, but a trade-off between privacy and fidelity (accuracy) needs to be considered.

While synthetic data tends to reduce privacy risks, it often will not eliminate them. There can namely be risks of re-identification (for instance via attacks) or that source data records appear in the synthetic dataset.

##### Differential privacy

Differential Privacy techniques add "noise" (small changes) to the original data to obfuscate certain details, while maintaining the explanatory power of the data.
This relies on a principle that small (differential) changes to individual entries do not significantly affect aggregate results. As such, robust aggregate information can be generated while reducing the how reliable individual elements are (hence protecting them).
These small changes can be added during data collection (distributed) or centrally ahead of data release (centralised).
Parameters (e.g. "how much noise?") still need to be chosen to obtain the relevant trade-off between privacy protection and utility. Work on evaluation is also needed.

##### Zero-knowledge proofs (ZKP)

Zero-knowledge proofs can be used to answer whether something is true or not based on information contained in a dataset, without disclosing the underlying dataset itself (e.g. is a given person over 21). 
This can mean for instance that for an organisation to answer a query it has, data subjects do not need to submit sensitive information but rather have the organisation verify the claim.
These technologies are still in their early development phases.

#### Encrypted data processing tools

##### Homomorphic encryption (HE)

Homomorphic encryption is a tool that makes computations based on encrypted data. This contrasts with standard data processing approaches where data needs to me made visible to the data processor.
The data subject encrypts the data with a key, sends it over to the data processor who will perform computations on the still-encrypted data that return an encrypted output, and this is returned to the data subject who can then unlock the data with the key.

For now, HE is less efficient than standard processing, requiring more computational power and time. It us used in small use cases.

##### Multi-party computation (MPC)

Multi-party computation are tools that allow a set of parties to jointly compute a function or transformation over their respective source data while keeping that source data private. Namely, it can aggregate sensitive data without the need for any single party to disclose their own data.
It removes the need for a trusted third party.
HE techniques are increasingly used in MPC.

##### Private set intersection (PSI)

Private set intersection (PSI) is a type of secure MPC that allows data subjects to identify common elements in their datasets without the need to reveal further contents or other elements of those datasets.
PSI has high maturity as a HE and MPC. It has been used for large-scale applications such as Covid-19 contact tracing or contact discovery in mobile apps.

##### Trusted Execution/Research Environments (TEE/TRE)

TEEs are a purpose-built area that provides processing capabilities separate from the operating system (OS), securely.
This area will hold sensitive, non-modifiable data against which secure code can be run.
It is designed such that the operating system cannot access information or read secrets, driven by a default working assumption that the OS is unsecure.

#### Federated and Distributed Analytics

##### Federated Learning

Traditionally, data analysis foresaw that linkage and processing would apply to a single centralised dataset (in turn created from datasets of the various data subjects).
With federated learning, raw data is preprocessed by each data subject (data source), with only the summary statistics or learnt parameters passed on to the data processor. These are then assembled with similar summary statistics or model parameters from other data subjects.
In this way, raw sensitive data does not leave the data subjects and does not need to be stored by the data controller or processor.
While this technique is widely deployed by some organisations, there are concerns that features may still reveal private information in some cases or that attacks could reveal the originating data.

##### Distributed analytics
[revisit]
In distributed or decentralised analytics, the data is housed by the data controller in a central location but the analysis or model training is distributed across multiple nodes.
It often requires common data models to be developed and coded first, to promote interoperability and reuse. With distributed analytics, software and tools can be deployed to where the data is located, as opposed to transferring data to a central repository.
In this approach data processors and analysts cannot directly access the data.

####  Data Accountability tools

##### Accountable Systems

Systems that promote the management of how data is collected, processed, analysed and shared and that track compliance. This includes visibility but also rule-, regulation- and user-based control.
These systems are still in early pilot, so are not ready for implementation. Distributed ledger technologies are one of the main technologies that could be leveraged in the future, though they come with their own risks.

##### Threshold Secret Sharing (TSS)

Threshold Secret Sharing is where a certain preagreed number (rather than typically one) and type of keys need to be used to unlock encrypted data. In this way, thresholds are set before data can be accessed.
For now, applications are narrow though and require large overhead if used on large datasets.

##### Personal Data Stores (PDS)

Personal Data Stores give control to individuals in deciding at a granular level how their data is stored, accessed, processed and disseminated. This enforces individual data portability rights and agency.
PDS switches the paradigm from the traditional data processing approach, which requires organisations to collect information from individuals and store them in large datasets for processing.
Most deployments are still in pilot stages. Other behavioural barriers also need to be addressed.

### Useful links

OECD (2023), "Emerging privacy-enhancing technologies: Current regulatory and policy approaches", OECD Digital Economy Papers, No. 351, OECD Publishing, Paris, [https://doi.org/10.1787/bf121be4-en](https://doi.org/10.1787/bf121be4-en).

ICO (2022), "Chapter 5: Privacy-enhancing technologies (PETs) - Draft anonymisation, pseudonymisation and privacy enhancing technologies guidance", ICO, accessed [here](https://ico.org.uk/media/about-the-ico/consultations/4021464/chapter-5-anonymisation-pets.pdf).

Royal Society (2023), "From privacy to partnership - The role of privacy enhancing technologies in data governance and collaborative analysis", The Royal Society, accessed [here](https://royalsociety.org/-/media/policy/projects/privacy-enhancing-technologies/From-Privacy-to-Partnership.pdf?la=en-GB&hash=4769FEB5C984089FAB52FE7E22F379D6).
