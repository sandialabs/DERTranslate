# DERTranslate

## Description
The code in DERTranslate library was developed by Sandia National Laboratories under funding provided by the U.S Department of Energy (DOE) Cybersecurity, Energy Security, and Emergency Response (CESER) as part of the project titled "DER NIDS Application Layer Maps to Extract Real-Time Physical and Control Data" Agreement Number 40986. 

This is an open-source software tool that generates standardized JSON-based maps (files) for IEEE 1547-2018 compliant DER systems to be input into Network Intrusion Detection System (NIDS) tools to capture physical data and control information. These maps translate register numbers to information-rich physical features, that can be used for downstream threat detection tasks (for instance, rule-based IDSs or Machine Learning (ML)-based IDSs). 

The contributor of this codebase is George Fragkos.
Questions or inquiries can be directed to George Fragkos (Sandia National Laboratories) at [gfragko@sandia.gov](mailto:gfragko@sandia.gov) 

## Installation and Usage
1. First you should install the dependencies using pip3 (note: depending on your access you may need to perform the following commands using sudo):
```console
pip3 install openpyxl
pip3 install json
pip3 install re
```

2. The you can download any DER PICS file of any DER manufacturer here:[SunSpec Certified Registry](https://sunspec.org/certified-registry/), and save it in the DERTranslate directory.

3. Then run the der_translate.py with passing as an argument the PICS file, which is going to be an .xlsx file:
```console
python3 der_translate.py <pics_example>.xlsx
```

where instead of <pics_example>.xlsx you will use the name of the file that you downloaded from the SunSpec Certified Registry.

4. A new directory will be created where it will include
   a) The .json map file of the DER device including all the different models (e.g., nameplate, etc.).
   b) The raw .json files for each separate models.

