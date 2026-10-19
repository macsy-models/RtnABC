# RtnABC: Detection of Rtn Toxins with MacSyFinder

This set of MacSyFinder models is dedicated to the genomic detection of **Rtn toxin complexes**, a novel family of polymorphic toxins secreted via the **Type IX Secretion System (T9SS)** in *Bacteroidota*. Rtn toxins are involved in **interbacterial competition** and **kin discrimination**, contributing to niche exclusion and competitive fitness.

---

## **About Rtn Toxins**

Rtn toxins are **Rhs repeat-containing polymorphic toxins** secreted by environmental *Bacteroidota*, particularly in the genus *Chryseobacterium*. These toxins form **molecular cocoons** composed of three proteins:
- **RtnA**: Contains a β-propeller domain fused to a **T9SS C-terminal secretion signal (CTD)**.
- **RtnB and RtnC**: Assemble into a cocoon encapsulating a **cleavable C-terminal toxic domain**.

Upon proteolytic cleavage, the toxic domain is released, targeting **closely related bacterial strains** to outcompete them. Rtn toxins act synergistically and shape bacterial competition in ecological niches.

---

## **Publication**
The Rtn toxins and their detection via MacSyFinder are described in:

> **Grandjean, M.**, Rudgalvytė, M., Delobelle, T., Elomari, M., Marchal, N., Oms, T., Paillat, M., Dieu, M., Cascales, E., Varoquaux, N., Abby, S. S., Fronzes, R., Doan, T., & Jurėnas, D. (2026).
> **"Rhs toxin complexes secreted via the type IX secretion system mediate kin discrimination in environmental Bacteroidota"**
> *Submitted manuscript*.

---

## **Installation and Usage with MacSyFinder**
To detect Rtn toxin complexes in bacterial genomes, first install MacSyFinder and the **RtnABC** model package, then run it on the protein file corresponding to your genome of interest:

### **1. Install MacSyFinder**
Ensure `macsyfinder` is installed (version 2.0 or later). This will also install the `msf_data` tool for managing model packages. See [here for Installation intructions](https://github.com/gem-pasteur/macsyfinder). 

### **2. Install the RtnABC Model Package**
```bash
msf_data install RtnABC
```

### **3. Run the search**

```bash
macsyfinder --db-type ordered_replicon \
    --sequence-db myproteins.fasta \
    --models RtnABC all
```

See [MacSyFinder's documentation](https://macsyfinder.readthedocs.io/en/latest/) for the description of more options available with MacSyFinder. 

## **References**

- For MacSyFinder:

> Néron, B., Denise, R., Coluzzi, C., Touchon, M., Rocha, E. P. C., & Abby, S. S. (2023). 
> MacSyFinder v2: Improved modelling and search engine to identify molecular systems in genomes. 
> *Peer Community Journal, 3, e28. [DOI:10.24072/pcjournal.250](https://doi.org/10.24072/pcjournal.250)*

> Abby, S. S., Néron, B., Ménager, H., Touchon, M., & Rocha, E. P. C. (2014). 
> MacSyFinder: A Program to Mine Genomes for Molecular Systems with an Application to CRISPR-Cas Systems. 
> *PLoS ONE, 9(10), e110726. [DOI:10.1371/journal.pone.0110726](https://doi.org/10.1371/journal.pone.0110726)*

- For Rtn Toxins:

> Grandjean, M., Rudgalvytė, M., Delobelle, T., Elomari, M., Marchal, N., Oms, T., Paillat, M., Dieu, M., Cascales, E., Varoquaux, N., Abby, S. S., Fronzes, R., Doan, T., & Jurėnas, D. (2026). 
> Rhs toxin complexes secreted via the type IX secretion system mediate kin discrimination in environmental Bacteroidota. 
> *Submitted manuscript*.
