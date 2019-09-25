# Docs as Code with Sphinx

This is an implementation of the Docs like Code approach to write and publish documentation using a static site generator (Sphinx).

## Table of Contents

- [Introduction](#introduction)
  - [How We Implement Docs as Code](#how-we-implement-docs-as-code)
- [Local Installation](#local-installation)
  - [Prerequisites](#prerequisites)
  - [Install](#local-installation)   
  - [Add New Content to the Documentation Site](#add-new-content-to-the-documentation-site)
- [Tests](#tests)
  - [Missing Links](#missing-links)
- [Continuous Deployment](#continuous-deployment)
  - [Netlify](#netlify)
 

## Introduction

*Docs as Code* is doing software documentation in the same way we do software development. We use the same tools that are used in software development—IDE, Git, and CI/CD—to write and publish a project's documentation. As a result, we deliver the documentation in the same way we deliver software.

### How We Implement Docs as Code

To deliver documentation as code, we follow a similar workflow as software development:

-  **Step 1. Create our documents as plain text files and use a Markup language.**  
We write our docs in reStructuredText.
-  **Step 2. Use an IDE to edit our documents.** 
We use Pycharm to edit all of our files.
-  **Step 3. Use a static site generator.** 
We use Sphinx. 
-  **Step 4. Use Git for file management and collaboration.** 
-  **Step 5. Test our documents.** 
We check for missing links.
-  **Step 6. Build and publish the documentation site continuously.**  
We adopt Continuous Integration (CI) and Continuous Development (CD) to deliver our documentation on a web server. We automatically deploy our documentation site after every commit we make.


[⇧ back to top](#table-of-contents)

## Local Installation

Instructions to set this project up on you local machine.


[⇧ back to top](#table-of-contents)

### Prerequisites

You need to install [Anaconda](https://www.anaconda.com/distribution/) and [Pycharm](https://www.jetbrains.com/help/pycharm/installation-guide.html).


[⇧ back to top](#table-of-contents)

### Install 
To set this project up on your local machine:

1.Clone this repo:
   ```
    git clone https://github.com/lilianabs/docs-as-code.git
   ```

2.Create a *conda* `docs-as-code` environment:

   ```
    conda create --name docs-as-code python=3.7 -y
   ```

3.Activate the `docs-as-code` environment:

   ```
     conda activate docs-as-code
   ``` 

4.Install the project dependencies:

   ```      
      while read requirement; do conda install --yes $requirement; done < requirements.txt
   ```
5.Open the project in Pycharm with `docs-as-code` interpreter.

[⇧ back to top](#table-of-contents)

### Add New Content to the Documentation Site

To add new content to the documentation site:

1.Add the new content as an *.rst* file to the `source` directory.

2.Build the documentation site:

   ```
    make html
   ```
   >Note: Execute the above command in the *docs-as-code* directory.

3.Got to the `html` directory:

   ```
    cd build/html
   ```

4.Start a Python local server to see the documentation site:

   ```
    python -m http.server
   ```
5.Go to `http://0.0.0.0:8000/` to see the documentation site.

>Note: Run command `make clean` to clean the project.
## Tests

We run a few scripts to check missing links and other aspects of the documentation.

[⇧ back to top](#table-of-contents)

### Missing Links

To check for missing links, run the script:

```
bash ./scripts/linkcheck.sh
```

[⇧ back to top](#table-of-contents)



## Continuous Deployment

We deploy this site to [Netlify](www.netlify.com).

### Netlify

1.Fork this repository.

2.Go to [Netlify](www.netlify.com).

3.Get a free account.

4.Click **New Site from Git**.

5.Click **GitHub**.

6.Click **Authorize Netlify**.

7.Enter your GitHub password.

8.Choose your forked repository.

9.Click **Deploy site**.

[⇧ back to top](#table-of-contents)