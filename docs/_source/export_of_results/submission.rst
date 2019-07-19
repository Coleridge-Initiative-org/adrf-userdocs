Submit an Export Request
================================================

Please read the export guidelines carefully and make sure your code and the material (files, tables, graphs, etc.) which you want to export is in compliance with it. Once the material you want to export is ready you can initiate an export request. There are three steps, detailed below, which you will need to complete to submit an export request: (1) prepare your export request, (2) submit your export request, and (3) create a merge request on GitLab for your export request. You will find two icons on your desktop to initate the request. 

.. image:: images/icons.png
  :width: 400
  :alt: Prepare and Submit icons


Prepare Export
^^^^^^^^^^^^^^^^^^

Start your export by clicking on the  "PrepareExport" icon on your desktop. This will open following terminal window:

.. image:: images/prepare.png
  :width: 400
  :alt: Terminal Window Prepare Export

The window shows all the projects you are a member of listed with a number. Please select the project you want to export files for by typing the number associated with this project and press enter. The prepare export script then clones your export repository (if necessary) and generates a new branch for the export which is named "export-username-YYYYMMDD". 

The export folder connected the the repo is located in your home directory. If you are a member of multiple projects, each project has its own export folder. You will find two subfolders "input" and "output" in the export folder.

.. image:: images/folders.png
  :width: 400
  :alt: Content of the Export folder

Now you can drag and drop the files you want to export in the corresponding folders:
* Input folder: please save all files you used to create the files you are asking to export. This includes all code files and any other documentation you want to provide with your results.
* Export folder: all files that you want to export go in this folder. Any format is allowed. Please remember that if you request graphs we need a csv or txt file showing the numbers behind the graph. If you want to export a juypter notebook please clear any data in the notebook before exporting.

When you are done with copying the files needed for the export you can close the windows and start the second part of the export request, the actual submission.  

Submit Export
^^^^^^^^^^^^^^^^^^^^^^^^

After preparing the export you need to click on the icon "SubmitExport" which will open following terminal window for you:

.. image:: images/submit.png
  :width: 400
  :alt: Terminal window after runnning prepare export

As in the export preparation you will have to make a decision for which project you want to submit the request. Enter the number associated with the project you want to submit. Then you will be asked to enter your user name and password for GitLab.

After entering your GitLab account info your export request will be pushed to the respective project export folder and GitLab will open so you can complete the export. The export request is labeled with "export-username-date".

Create Merge Request
^^^^^^^^^^^^

In order to complete your export request and notify ADRF you need to submit a merge request through GitLab. The following screenshots will walk you through the submission of a merge request.

### 1. Create a New Merge Request
GitLab will open directly on the merge request tab. Please always click "New Merge Request", not the blue box which says Create Merge Request.

.. image:: images/gitlab2.png
  :width: 400
  :alt: Merge Request tab in gitlab

### 2. Select the Correct Branches
Now you have to select the source and target branch.

.. image:: images/gitlab3.png
  :width: 400
  :alt: Merge Request branch selection in gitlab

* The source branch field on the left shows the name of your export project repository. The right field shows the export you submitted. If you click on it it will open a drop down menu. Please select the most recent submission you want to export ("export-username-date").
* The target branch field on the left should display the same project repository as in the source branch field. Master should be selected on the right field.

Please make sure that you selected the correct branches before you click "Compare branches and Continue".

### 3. Fill out the Form and Submit the Request
Now you can complete the export form and click "Submit Merge Request":
* Title: Please fill in the title with "export-username-date"
* Description: Please provide us with a description of what you are exporting. The more details you provide the easier it is to understand what you did in your analyses. Think about the information someone who is not familiar with your project needs to know to understand your research.
* Assignee/Milestones/Labels: You can leave these fields as they are
* Source branch: Should be the branch that you submitted for export ("export-username-date")
* Target branch: Please make sure that master is selected.

.. image:: images/gitlab4.png
  :width: 400
  :alt: Fill out mere=ge request form in gitlab

Please do not close the merge request. If you close the merge request the ADRF staff will not be notified that there is an export request in line to be disclosure proofed. 

Download Approved Export
^^^^^^^^^^^^^^^^^^

Now the export was submitted and is in line for disclosure review. During the disclosure review ARDF staffs makes sure that all the output you wnat to export does not re-identify a single data entity and is prepared according to the export guidelines. The ARDF will be in touch with you and send you a download link if your export is approved. If your export is not approved ADRF staff will reach out to you and let you know what you need to change to get your export approved. The export request will be protected and you can not make any changes to this export request. If you need more output you need to submit a new export request.

We will try to make export turnaround as fast as possible, but in order to do that, it will be necessary to keep the number of the export requests at a minimum.
