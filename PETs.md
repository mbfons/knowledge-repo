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

* **Encrypted data processing tools**: tools that allow data to remain encrypted during use.

    * Types: e.g. homomorphic encryption; multi-party computation; trusted research environments / secure data environments
    * Advantages: data does not need to be decrypted before use
    * Cautions: computation and infrastructure costs, data quality ...

* **Federated and distributed analytics**: tools or procedures that allow analytical actions to be run on data, but where the data is not visible or accessible while executing those actions.

    * Types: e.g. federated learning protocols
    * Advantages: microdata does not need to be shared by parties to allow for insights; scalability
    * Cautions: computation and infrastructure costs, connectivity, information on data models and interoperability
 
* **Data accountability tools**: tools that seek to enhance data protection and privacy by allowing for data subjects to have control over their own data. Not strictly a PET since their primary aim is not data confidentiality itself but rather control and accountability. 

    * Types: e.g. personal data stores, accountable systems
    * Advantages: user control and transparency
    * Cautions: low maturity and technology readiness of tools; narrow scope use cases; few standalone applications; not strictly a PET

PETs tend to not be standalone tools, but rather used together with other PETs or other organisational tools to achieve data governance objectives.

### Useful links

OECD (2023), "Emerging privacy-enhancing technologies: Current regulatory and policy approaches", OECD Digital Economy Papers, No. 351, OECD Publishing, Paris, [https://doi.org/10.1787/bf121be4-en](https://doi.org/10.1787/bf121be4-en).

ICO (2022), "Chapter 5: Privacy-enhancing technologies (PETs) - Draft anonymisation, pseudonymisation and privacy enhancing technologies guidance", ICO, accessed [here](https://ico.org.uk/media/about-the-ico/consultations/4021464/chapter-5-anonymisation-pets.pdf).

Royal Society (2023), "From privacy to partnership - The role of privacy enhancing technologies in data governance and collaborative analysis", The Royal Society, accessed [here](https://royalsociety.org/-/media/policy/projects/privacy-enhancing-technologies/From-Privacy-to-Partnership.pdf?la=en-GB&hash=4769FEB5C984089FAB52FE7E22F379D6).
