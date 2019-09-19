Docs as Code
=======================
In this article we explain what is **Docs as Code** and give a general overview on how to implement it.

What is Docs as Code?
-----------------------
*Docs as Code* is doing software documentation in the same way we would do software development. We use the same tools that are used in software development—IDE, Git, and CI/CD—to write and publish software documentation. As a result, we deliver the documentation in the same way we deliver software.

How To Implement it?
-----------------------
To deliver documentation as code, we follow a similar workflow as software development:

#. **Step 1. Create your documents as plain text files.** We use a markup language such as Markdown, reStructuredText, or Asciidocs.

#. **Step 2. Use an IDE to edit your documents.** For example, we can use *vs code* or *Atom* but any simple text editor works.

#. **Step 3. Use a static site generator to create *html* files of your documentation.** There are many static site generators out there. The most popular ones are: Sphinx, Hugo, and Jekyll but we can choose whichever adapts best to our needs.

#. **Step 4. Use Git for file management and collaboration.** As we develop the documentation of a software product, we need to keep track of the different changes we do to the documentation. This is most useful when we're working as part of a team.

#. **Step 5. Test your documents.** We run validation scripts to make sure that we follow a style guide or that our vocabulary is consistent across our documentation. Also, we check that there are no missing links in our documentation site.

#. **Step 6. Build the documentation site and publish continuously.**  We adopt Continuous Integration (CI) and Continuous Development (CD) to deliver our documentation on a web server. We automatically deploy our documentation site after every commit we make.

We might *not* follow all of the above steps. Maybe, we deliver our documentation not in a web server but as single html files. We might prefer to only test for missing links. Hence, we can follow the steps that best suit our project's needs.


