========
Concepts
========

In this section, we introduce the basic concepts and terms in the Big Data Processor (BDP) system.

User Roles
==========
There are different aspects to use Big Data Processor.

Based on different user roles, we categorized these roles into 1) users, 2) developers, and 3) administrators.
The users execute tasks without changing task settings.
The developers not only execute tasks but also construct tasks/workflows into packages.
The administrators can manage users and do all the above mentioned actions.
BDP provides basic user priviledges for the above user roles. Please see the administration sections.



Usage Pattern
=============

As shown in the following figure, a Project contains DataFiles and Results, 
while Task definitions and customized Pages are stored in a Package.
Projects are created by users and Packages are created by developers.
A basic usage cycle may start by creating a project with selected packages.
Users can upload required files to this project and these files become DataFiles.
Then, users can execute tasks that belong to the selected packages.
After setting the tasks parameters, the task can be executed and all provenance of this task is stored as a Result. 

A Result records task status, parameters including input/output files, 
the runtime configurations, standard output/error, the task commands, the running time and all related information.
You may see the Results as histories. Everything that relates to each task execution is recorded in a Result.
After task executions, new DataFile records may be created in the Project and these DataFiles may be used as inputs of another task.
In this way, we may execute a workflow manually.

In fact, a workflow-typed Task can be easily constructed by piping other Tasks.
We provide web interfaces that allow developers to concatenate Tasks by just mouse clicks and drag-and-drops.
If users execute the workflow-typed Task, the Result records the progress and all sub-Tasks of the workflow as children Results.


Task Definition Language
========================
To further ease the task definitions on web, we developed a new task definition language, the Workflow Playbook.
The workflow playbook is a concise task configuration format for fast and portable workflow constructions.
It is written in the `YAML <http://yaml.org/>`_ format and is inspired by the `Ansible Playbook <https://docs.ansible.com/ansible/latest/user_guide/playbooks.html>`_.
With the templating concept, we can simplify the workflow definitions. It is desinged to be human-readable format.

Compared to the `Common Workflow Language (CWL) <https://www.commonwl.org/>`_, workflow playbook is more concise and easy to write.
The CWL is also written in the YAML format and provides detailed configurations to define tasks and workflows. 
We believe that the workflow definitions can be more concise through templating, instead of verbose configurations.
Besides, we can easily write for-loops or do if-else conditions via templating while the CWL currently hasn't supprted them.

We expect this concise format is easy enough for non-expert people to understand and write without learning additional domain-specific languages.
In addition, this workflow playbook is seamlessly integrated on the Big Data Processor so that we can write the worklfow playbook directly on the web page.



Portable workflow execution
===========================
To enable portable workflow executions, we apply the container techniques.
Each task of a workflow is encouraged to executed in a container, such as Docker or Singularity.
A container carries its good runtime environemnts.
The dependent libraries or the required tools can be pre-installed in side the container image.
We can say that tasks can be guaranteed to be executed successfully inside the well-defined container environment.
Therefore, the task is portable.

When executing the containerized tasks, the defualt behaviors of BDP will mount two folders to the container.
The Project and Package folders on the host will be mounted to ``/project`` and ``/package`` inside the container.

We encourage that containers contain only the required environments such as libraries or tools, 
and task scripts in the Package folder are mounted right before task executions.
BDP provides web interface to allow developers to edit task script files. In this way, 
developers can edit their scripts and execute them directly without updating container images.




Project
=======
A Project is a collection of DataFiles and Results. 
Under the hood, a project is a folder that stores all the DataFiles. The Results information is mainly stored in databases.




.. Project, DataFile, Results, Package, Task, 


DataFile
========


Result
======

Package
=======


Task
====


Page
====
