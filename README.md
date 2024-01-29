# getting-started
This repository is you're go-to repository for  accessing project templates, documentation, code styling guides and minimum viable code examples.

Follow the list of checks below to ensure that you are developing software development initiatives that abide by Zutari's best practice, styling and project structure:
- [X] Use Git-workflows to version control and structure your development to have the correct branching structure. Regularly push new features and updates to the correct branch (at least weekly or every Friday). External training resources can be accessed from the Zutari-CoDe Sharepoint page.
- [X] Use a folder template that matches as close as possible to the guidelines.
- [X] Study and implement the coding standards. This ensures easy readability by different developers and consistency across code bases. Utilise industry best practice.
- [X] Implement a [Software Design Document](#software-design-document-template) for a project to clearly state the requirements and expectations.
- [X] The final implementation phase used for a project is externalisation - where the end user utilises a specific tool. This might be a simple, standalone tool or script, such as a Dynamo file, or a fully fledged piece of software with a GUI (graphical user interface). Consider how the tool be deployed in a production environment, considering limitations imposed on administrative rights. Refer to the [Virtual Machine](#virtual-machines) resources that are available on GitHub.
  
## Project Management
TODO: Talk about the project management resources available from Github.

## Virtual Machines
TODO: Study the availability of complementary computational resources made available by Github.

## Git Workflow
TODO: Add information here.

## Unit testing and integration
TODO: Add information here.

## Project folder structure
Insofar possible, we recommend using the file structure convension as detailed below for consistency (adapted from the [Coockiecutter Data Science](https://drivendata.github.io/cookiecutter-data-science/) blog). Note that every repository is limited to 500MB of storage capacity - GitHub does not replace Sharepoint, but provides enough capacity to host some test files or data that should form apart of unit testing and integration. Ensure existing standards, e.g. APIMS (Aurecon Project Information Management Standard) is followed for handling data received and transmitted for projects.

TODO: Create folder templates and sync to the repository that users can use as a template

### Python
```
├── LICENSE              <- TODO: Finalise license definition. all IP associated with projects is retained by Zutari 
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

Google provides another excellent [Python Style Guide](https://google.github.io/styleguide/pyguide.html) that can be followd, overlapping with the existing Python guidelines.

TODO: Andre to adapt and coding guidelines avaialble from the Aurecon CoDe team.
TODO: Andre to either adapt or link in Paul's coding guidelines.

## Software Development Guidelines
Zutari is in the process of finalising the software development guidelines to abide by when creating or writing software, scripts,
extensions of add-ins. This is expected to be finalised during Q1 2024 (contact point: Andre Broekman, Timothy Carolus)

## Software Design Document Template
The software design document template is designed by ArjanCodes, a lecturer and software developer. Spending enough time during the initial stages of the project to plan out the requirements, implementation and deliverables is a paramount to the successful execution and maintainability of a project. The 7-step template below aligns with the Computational Design (CoDe) philosophy and should be used as part of the documentation process, with each heading answered in a clear and concise manner.

1. **About**
   1. What is the software application or feature?
   2. Who's it intended for?
   3. What problem does the software solve?
   4. How is it going to work?
   5. What are the main concepts that are involed and how are they related?
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
