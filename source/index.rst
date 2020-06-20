.. Big Data Processor documentation master file, created by
   sphinx-quickstart on Wed Aug  1 10:37:11 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Big Data Processor's documentation!
==============================================
Big Data Processor (BDP) is a light-weight, yet complete and scalable workflow platform.
This web workbench mainly focuses on the workflow **portability**, **reproducibility** and **reusiblity**.
It is generic so that workflow builders can freely design their workflows into portable packages.

Additinally, it supports **portable data visualizations**.

Most workflow management systems mainly help us to execute and monitor workflows.
After that, users offten have to find their way to explore results.
Here, in this workbench, workflow builders are allowed to freely develop web pages for their workflows 
both to provide guidance for workflow executions and to provide interactive data visualizations.

With these customized web pages, 
users can visualize results interactively right after workflow executions.


The goal is to make **All on web pages!**.

This web workbench provides web interfaces that covers project management, workflow executions, task monitoring, and package building.
Packages of BDP are in a portable format that can be installed on every BDP hosts by just mouse clicks.
Then, these workflows in the packages are ready to run with near-zero configurations!

The coolest part is that our Page system also provides the web proxy functionality.
Our Page system can not only serve the above mentioned customized web pages, but can also serve containerized web services or even desktop applications, such as R/Shiny apps, RStudio, Jupyter Notebook or Matlab IDE and many more!

.. toctree::
    :maxdepth: 1

    Installation<installation>
    Getting Started<getting-started>

.. toctree::
    :maxdepth: 4
    :caption: Introduction

    Concepts<introduction/concepts>
    System Architecture<introduction/system-architecture>

.. toctree::
    :maxdepth: 4
    :caption: Basic usages

    Manage projects
    Import files
    Execute tasks
    Collect results

.. toctree::
    :maxdepth: 4
    :caption: Package management

    Install packages
    Configure runtime configurations
    Task definitions
    Workflow Constructions
    
    
.. toctree::
    :maxdepth: 4
    :caption: Workflow Playbook

.. toctree::
    :maxdepth: 4
    :caption: Entry Page



.. toctree::
    :maxdepth: 4
    :caption: Task Adapter

.. toctree::
    :maxdepth: 4
    :caption: Quick Start

    Full steps to construct a pipeline<tutorials/tutorial-full-step-pipelines>
    Task deployment on Google Cloud Platform<tutorials/tutorial-task-deploy-GCP>
    Non-root MongoDB Installation<tutorials/mongodb-non-root-installation>



.. For users<web-interface/the-web-interface-user>
    For administrators<web-interface/the-web-interface-admin>
    For pipeline developers<web-interface/the-web-interface-pipeline-dev>



.. Best practice to plan your tasks<pipieline-development/task-best-practice>
    Manage Packages
    Define Tasks<pipieline-development/task-definition>
    Pipe your Tasks into workflows
    Customized Pages for your workflows
    Building package container<pipieline-development/bdp-package-container>
    Create your package list<pipieline-development/create-package-registry>

.. toctree::
    :maxdepth: 4
    :caption: System Administrations

    User managment
    Package settings
    Enable Google 3rd party sign-in<administration/allow-google-sign-in>
    Enable Google reCAPTCHA



Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

