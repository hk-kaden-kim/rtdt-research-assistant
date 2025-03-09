<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
<!-- [![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![LinkedIn][linkedin-shield]][linkedin-url] -->

[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]


<!-- PROJECT LOGO -->
<br />
<div align="center">
<!--   <a href="https://github.com/RTDT-LABORATORIES/Algorithms/tree/main/Report_Generation">
    <img src="./Logo_rtdt_logo_v2.png" alt="Logo">
  </a> -->

<h3 align="center">Report Generation Toolkit v1.0</h3>

  <p align="center">
    A toolkit to generate PDF report following RTDT report Latex format.
    <br />
    <a href="https://github.com/RTDT-LABORATORIES/Algorithms/tree/main/Report_Generation"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <!-- <a href="https://github.com/github_username/repo_name">View Demo</a> -->
    ·
    <a href="https://github.com/RTDT-LABORATORIES/Algorithms/milestone/5">Report Bug</a>
    ·
    <a href="https://github.com/RTDT-LABORATORIES/Algorithms/milestone/5">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project">About The Project</a></li>
    <li><a href="#getting-started">Getting Started</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#version-history">Version History</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Toolkit

[![Product Name Screen Shot][product-screenshot]](https://github.com/RTDT-LABORATORIES/Algorithms/blob/main/Report_Generation/RTDT_ReportGen_Toolkit_v1_0/pdf_samples/sampleReport0.pdf)

Report generation is always important to track and save the result of model training, model evaluation, data analysis and techno-commercial white papers. However, it is also very tedious and repetitive works to users. So, we create 'RTDT report generation toolkit' to generate automatically RTDT report in pre-designed form and be compatible with other RTDT workflows.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



### Built With
Python
* [Jinja2][Jinja-url]
* [PyYAML][PyYAML-url]
* (Optional) [Essential-Generators][EssGen-url]

Latex
* [TeX Live][TeXLive-url]
* [pdfTeX][pdfTeX-url]


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started
```sh
# Install Python pacakages.
$ pip install -r ./RTDT_ReportGen_Toolkit_v1_0/requirements.txt
```

### LateX Environment
This toolkit uses pdfTeX to complie LateX files into pdf file. So, before utilizing this toolkit, ensure that pdfLateX is installed on your machine.

```sh
# Check pdfTeX on your machine.
$ pdflatex --version
pdfTeX 3.141592653-2.6-1.40.24 (TeX Live 2022)
...
```

If pdfLateX is not installed on your machine, follow the installation guidline of [TeX Live][TeXLive-url]. pdfLateX(pdfTeX) is released as part of [TeX Live][TeXLive-url].

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage
### About the Latex folder
The files inside the __Latex__ folder are main source for RTDT report pdf output. It consist of the LateX template, and the report yaml file including figures and text contents. If user want to change the Latex template or do some final touch for generated Latex files, please try to edit the files at this folder.

    ├── Latex
    │   ├── contents
    │       ├── figures
    │           ├── Logo_rtdt_logo_v2.png
    │           ├── ...
    │       ├── reportout.yaml
    |
    │   ├── templates
    │       ├── template_main.tex
    │       ├── template_section.tex
    │       ├── ...
    │
    │   ├── sections
    │       ├── ...
    │
    │   ├── latexmkrc
    |   ├── main.tex
    |   ├── preambule.sty

#### Folder | contents
This folder includes all contents which will be written on the RTDT report. The image-based contents(e.g., figure) are saved into the subfolder _./figures_. the text-based contents(e.g., textbox, table, ordered list) and its structure are defined in [_reportout.yaml_][reportout-YAML-url]. For the details of this file, please refer to [_info_reportout.txt_][reportout-info-url].

#### Folder | templates (Edit only when it is neede)
This folder includes designated format of LateX file. Jinja2 environment variables and structures helps rendering the contents of report written in [_reportout.yaml_][reportout-YAML-url]. For the details of how to create/edit template_*.tex, please refer to [_info_template.txt_][template-info-url].

#### Folder | sections (Auto-generated by toolkit)
This folder includes all .tex files automatically generated by RTDT Report Generation Toolkit. Finally, these TeX files will be imported at the _../main.tex_ in order to organize the full report.

### Example
* A sample workflow of this toolkit can be found at [here][example-url]
* A sample pdf result of this toolkit can be found at [here][sample-pdf-url]
* Source code of this toolkit can be found at [here][source-code-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [ ] Build python library to create RTDT Report YAML.
- [ ] Support other types of RTDT Report format.
- [ ] Integrate into the RTDT user workflow.
- [ ] Error handling.

See the [open issues](https://github.com/RTDT-LABORATORIES/Algorithms/milestone/5) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- VERSION HISTORY -->
## Version History

- __07/09/2023 v1.0__ : _release RTDT Report Generation Toolkit v1.0 following the base spec. [reference](https://github.com/RTDT-LABORATORIES/Algorithms/issues/12)_

See the [open issues](https://github.com/RTDT-LABORATORIES/Algorithms/milestone/5) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- LICENSE -->
## License

Distributed under the Apache License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Kim, Hyeongkyun - [@hk-kaden-kim](https://github.com/hk-kaden-kim) - hyeongkyun.kim@uzh.ch

Abdallah, Imad - [@IAbda](https://github.com/IAbda) - abdallah@ibk.baug.ethz.ch

Project Link: [RTDT-LABORATORIES/Algorithms/Report_Generation](https://github.com/RTDT-LABORATORIES/Algorithms/tree/main/Report_Generation)

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[issues-shield]: https://img.shields.io/github/issues/github_username/repo_name.svg?style=for-the-badge
[issues-url]: https://github.com/RTDT-LABORATORIES/Algorithms/milestone/5
[license-shield]: https://img.shields.io/github/license/github_username/repo_name.svg?style=for-the-badge
[license-url]: https://github.com/RTDT-LABORATORIES/Algorithms/blob/main/LICENSE
[product-screenshot]: ./RTDT_Report_Toolkit_v1.0_sample.png
[Jinja-url]: https://jinja.palletsprojects.com/en/3.1.x/
[PyYAML-url]: https://pypi.org/project/PyYAML/
[EssGen-url]: https://pypi.org/project/essential-generators/
[pdfTeX-url]: https://ctan.org/pkg/pdftex
[TeXLive-url]: https://tug.org/texlive/
[reportout-YAML-url]: https://github.com/RTDT-LABORATORIES/Algorithms/blob/main/Report_Generation/RTDT_ReportGen_Toolkit_v1_0/Latex/contents/reportout.yaml
[reportout-info-url]: https://github.com/RTDT-LABORATORIES/Algorithms/blob/main/Report_Generation/RTDT_ReportGen_Toolkit_v1_0/Latex/contents/info_reportout.txt
[template-info-url]: https://github.com/RTDT-LABORATORIES/Algorithms/blob/main/Report_Generation/RTDT_ReportGen_Toolkit_v1_0/Latex/templates/info_template.txt
[example-url]: https://github.com/RTDT-LABORATORIES/Algorithms/blob/main/Report_Generation/RTDT_ReportGen_Toolkit_v1_0/Example.ipynb
[sample-pdf-url]: https://github.com/RTDT-LABORATORIES/Algorithms/blob/main/Report_Generation/RTDT_ReportGen_Toolkit_v1_0/pdf_samples
[source-code-url]: https://github.com/RTDT-LABORATORIES/Algorithms/blob/main/Report_Generation/RTDT_ReportGen_Toolkit_v1_0/RTDT_ReportGen_Toolkit.py
