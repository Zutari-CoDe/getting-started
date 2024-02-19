# getting-started
This repository is you're go-to repository for  accessing project templates, documentation, code styling guides and minimum viable code examples.

Follow the list of checks below to ensure that you are developing software development initiatives that abide by Zutari's best practice, styling and project structure:
- [X] Use Git-workflows to version control and structure your development to have the correct branching structure. Regularly push new features and updates to the correct branch (at least weekly or every Friday). External training resources can be accessed from the Zutari-CoDe Sharepoint page.
- [X] Use a folder template that matches as close as possible to the guidelines.
- [X] Study and implement the coding standards. This ensures easy readability by different developers and consistency across code bases. Utilize industry best practice.
- [X] Implement a [Software Design Document](#software-design-document-template) for a project to clearly state the requirements and expectations.
- [X] The final implementation phase used for a project is externalization - where the end user utilizes a specific tool. This might be a simple, standalone tool or script, such as a Dynamo file, or a fully fledged piece of software with a GUI (graphical user interface). Consider how the tool be deployed in a production environment, considering limitations imposed on administrative rights. Refer to the [Virtual Machine](#virtual-machines) resources that are available on GitHub.

## Project Management
Agile software development refers to a select set of generalized principles to abide by during the course of software development and project execution. We strive to embrace to what is conducive to our work environment that is uniquely adapted to address large-scale engineering projects, both locally as well as internationally.

### The Agile Manifesto
The [Manifesto for Agile Software Development](https://agilemanifesto.org/) uncovers better ways of developing software by doing it and helping others do it. Through this work we have come to value:
- **Individuals and interactions** *over* processes and tools.
- **Working software** *over* comprehensive documentation.
- **Customer collaboration** *over* contract negotiation.
- **Responding to change** *over* following a plan.

Whilst there is value in the items on the right, we value the items on the left more. 

### Principles
There are 12 principles behind the Agile Manifesto:
1) **Working software/product**: Working software is the primary measure of progress.
2) **Promote sustainable working**: Welcome changing requirements, even late in development. Agile processes harness change for the customer's competitive advantage.
3) **Attention to technical excellence**: Continuous attention to technical excellence and good design enhances agility.
4) **Simplicity is essential**: Simplicity--the art of maximizing the amount of work not done--is essential.
5) **Self-organizing teams**: The best architectures, requirements, and designs emerge from self-organizing teams.
6) **Regular self-evaluation**: At regular intervals, the team reflects on how to become more effective, then tunes and adjusts its behavior accordingly.
7) **Face-to-face interactions**: The most efficient and effective method of conveying information to and within a development team is face-to-face conversation.
8) **Continuous delivery of solutions**: Our highest priority is to satisfy the customer through early and continuous delivery of valuable software.
9) **Verifiability, reproducibility, maintainability**: Agile processes promote sustainable development. The sponsors, developers, and users should be able to maintain a constant pace indefinitely.
10) **Deliver value frequently**: Deliver working software frequently, from a couple of weeks to a couple of months, with a preference to the shorter timescale.
11) **Break silos**: Business people and developers must work together daily throughout the project.
12) **Motivated individuals**: Build projects around motivated individuals. Give them the environment and support they need, and trust them to get the job done.

### Project Management Tools
**IN PROGRESS**: GitHub provides built-in project management tools. Feel free to evaluate the tools to find what works best. Jira is currently being evaluated as a potential alternative, but this does require licenses (Rick and Andre currently trialing some features in collaboration with Zark Goosen and Christo Reeder).

## Codespaces (Virtual Machines)
**TODO**: Study the availability of complementary computational resources made available by Github.
Initial testing of Codespaces appears to work well for deploying small tools. The VM can stay persistent for up to four hours (15 minutes by default). 
A complimentary 160 core-hours are provided per month to experiment with.

## Git Workflow
Git - an acronym for global information tracking - is crucial for developing well maintained and functioning coding solutions. Version control provides the ability for multiple people to be working on the same project simultaneously, whilst maintaining coherence between different, often remote, instances of the codebase.

### Minimum required workflow (*dev-main*)
At a minimum, a *dev-main* branching strategy should be employed. Active development occurs on the *dev* branch, which is merged into the *main* branch once a stable and tested solution is developed. A fully functioning version repository should be maintained on the *main* branch that is used in production.

A more comprehensive git-workflow can be employed for a larger codebase, as is recommended by the Data Science team. This enables the development of new features, deploying quick bug fixes and testing new developments prior to release as a working version.

[<img src="https://nvie.com/img/main-branches@2x.png">](https://nvie.com/posts/a-successful-git-branching-model/).

### Software development workflow
For larger projects, branches can be created for main, development, features, releases and hotfixes.

[<img src="https://nvie.com/img/git-model@2x.png">](https://nvie.com/posts/a-successful-git-branching-model/).

## Software Testing
Software testing is the act of examining the artifacts and the behavior of the software under test by validation and verification. Not all scripts or applications will necessarily require unit tests, e.g. simple data processing. For OOP (object-orientated programming it is imperative to implement within a project).

**Unit tests** test individual units (modules, functions, classes) in isolation from the rest of the program.
**Integration tests**, as the name suggests, is to test whether many separately developed modules work together as expected.
Link for unit testing information: https://realpython.com/python-testing/

TODO: Develop example script that implement unit testing and integration in production.


## Project folder structure
Insofar possible, we recommend using the file structure convention as detailed below for consistency (adapted from the [Coockiecutter Data Science](https://drivendata.github.io/cookiecutter-data-science/) blog). Note that every repository is limited to 500MB of storage capacity - GitHub does not replace Sharepoint, but provides enough capacity to host some test files or data that should form apart of unit testing and integration. Ensure existing standards, e.g. APIMS (Aurecon Project Information Management Standard) is followed for handling data received and transmitted for projects.

TODO: Create folder templates and sync to the repository that users can use as a template

### Python
```
├── LICENSE              <- TODO: Finalize license definition. all IP associated with projects is retained by Zutari 
|                           or Zutari/Aurecon agreement in the case of the GDC.
├── README.md            <- The top-level README for developers using this project.
├── setup.py             <- Make this project pip installable with `pip install -e` (in the case of a module that is)
├── requirements.txt     <- The requirements file for reproducing the analysis environment, e.g.
│                           generated with `pip freeze > requirements.txt`. PyCharm has built-in tools for this.
│                           Anaconda will typically utilize a YAML configuration file or similar to specify the environment.
├── data
│   ├── external         <- Data from third party sources.
│   ├── interim          <- Intermediate data that has been transformed.
│   ├── processed        <- The final, canonical data sets for modeling.
│   └── raw              <- The original, immutable data dump. Don't ever edit your raw data, especially not manually,
│                           and especially not in Excel.
│
├── notebooks            <- Jupyter notebooks. Naming convention is a number (for ordering),
│                           the creator's initials, and a short `-` delimited description, e.g.
│                           `1.0-jqp-initial-data-exploration`.
│
├── references           <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports              <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures          <- Generated graphics and figures to be used in reporting.
│
└── src                  <- Source code for used for a project. 
    ├── __init__.py      <- Makes src a Python module. The __init__ file is used to import the file as a module.
    ├── main.py          <- Scripts to download or generate data  
    ├── data             <- Scripts to download or generate data
    │   └── make_dataset.py
    └── visualization    <- Scripts to create exploratory and results oriented visualizations
        └── visualize.py
```

## Coding standards
Zutari set out the initial coding guidelines for Python (written by Paul Nel). These sets out some good starting guidelines to aid 
in providing some measure of uniformity given the language's popularity.

Google provides another excellent [Python Style Guide](https://google.github.io/styleguide/pyguide.html) that can be followed, overlapping with the existing Python guidelines.

**TODO**: Andre to adapt and coding guidelines available from the Aurecon CoDe team.
**TODO**: Andre to either adapt or link in Paul's coding guidelines.

## Software Development Guidelines
Zutari is in the process of finalizing the software development guidelines to abide by when creating or writing software, scripts,
extensions of add-ins. This is expected to be finalized during Q1 2024 (contact point: Andre Broekman, Timothy Carolus)

## Software Design Document Template
The software design document template is designed by ArjanCodes, a lecturer and software developer. Spending enough time during the initial stages of the project to plan out the requirements, implementation and deliverables is a paramount to the successful execution and maintainability of a project. The 7-step template below aligns with the Computational Design (CoDe) philosophy and should be used as part of the documentation process, with each heading answered in a clear and concise manner.

1. **About**
   1. What is the software application or feature?
   2. Who's it intended for?
   3. What problem does the software solve?
   4. How is it going to work?
   5. What are the main concepts that are involved and how are they related?
2. **User Interface**
   1. What are the main user stories (happy flows + alternative flow)?
   2. If you’re adding a new feature to an existing software application, what impact does the feature have on the overall structure of the interface? (are there big changes in the organization of menus, navigation, and so on?).
3. **Technical Speficiations**
   1. What technical details need developers to know to develop the software or new feature?
   2. Are there new tables to add to the database? What fields?
   3. How will the software technically work? Are there particular algorithms or libraries that are important?
   4. What will be the overall design? Which classes are needed? What design patterns are used to model the concepts and relationships?
   5. What third-party software is needed to build the software or feature?
4. **Testing and Security**
   1. Are there specific coverage goals for the unit tests?
   2. What kinds of tests are needed (unit, regression, end-to-end, etc)?
   3. (new feature only) Are there any potential side-effects on other areas of the application when adding this feature?
   4. What security checks need to be in place to allow the software to ship?
   5. (new feature only) How does the feature impact the security of the software? Is there a need for a security audit before the feature is shipped?
5. **Deployment**
   1. Are there any architectural or DevOps changes needed (e.g. adding an extra microservice, changes in the deployment pipelines, adding secrets to services)?
   2. Are there any migration scripts that need to be written?
6. Planning
   1. How much time will developing the software or feature cost?
   2. What are the steps and how much time does step take?
   3. What are the developmental milestones and in what order?
   4. What are the main risk factors and are there any alternative routes to take if you find out something isn’t feasible?
   5. What parts are absolutely required, and what parts can optionally be done at a later stage? (i.e. the Definition of Done)
7. Broader Context
   1. What are the limitations of the current design?
   2. What are the possible extensions to think about for the future?
   3. Any other considerations?
