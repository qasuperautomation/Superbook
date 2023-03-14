---
title: Chapter 2 - Testing Documents
date: Last Modified
permalink: /qaguidance/content/index.htm
toc: true
eleventyNavigation:
  order: 10
  parent: QA Guidance
  key: Chapter 2 - Testing Documents
---
### **BACKGROUND**

The basic idea is to include regression testing (partially) during the feature testing period, this is the tactical preparation that is relevant to the faster release cycle when the regression period is being shortened. To start we can use the rule of thumb: “Check the blast radius of the changes”.

**WHAT IS TEST PLAN DOCUMENT ?**

**Test plan document** is a document which contains the plan for all the testing activities to be done to deliver a quality product. Test Plan document is derived from the Product Description, SRS, or Use case document for all future activities of the project, it’s usually prepared by Test Lead or Test Manager.

**Test plans** acts as a blueprint or instruction manual of how and what you will test for a product release or sprint. It defines the scope, schedule, approach, and resources for your testing efforts.

**Test plans** includes the kind of information that everyone needs throughout the product's journey to do their job efficiently.

**WHAT IS TEST STRATEGY ?**

Test Strategy are high-level documents and are usually developed by the PM (Project Manager). This type of documentation captures our approach to testing the product and achieving the goals. And usually comes from BRD or PRD. Documents such as the Test Strategy doc are project-base documents which can be modified according to the project domain and requirements.

**WHAT IS TEST SCENARIO ?**

Test Scenario means to give an idea of what we have to test (test). Test scenarios are like high-level test cases.

**WHAT IS TEST CASES ?**

Test cases are a collection of steps that can be executed positively and negatively from a test scenario that has a set of pre-conditions, test data (test data), expected results, post-conditions, and actual results. results).

**HOW TO WRITE EASY TEST CASES ?**

Typically, QA engineers use Excel sheets to manually write test cases. In addition, you can use test management tools, such as TestRail, xray, Test Link, Qtest to create and maintain test cases

![Example of a test case](https://ik.imagekit.io/kmv5uxk0b/qa_guidance/test_case_template_qa_guidance.png?updatedAt=1678775819503 "Example of a test case")

In making the test case at Aplikasi Super, the QA Analyst is required to fill in some data in the Header on the Excel Sheet::

1. Project/Application Name
2. Testing Date
3. Tester Name / Designation
4. Environment : Staging / Production

Then the QA Analyst performs some data entry to create a test case, which consists of:

1. Scenario ID
2. Testcase ID
3. Jira ID /Gitlab ID
4. Testcase Description
5. STP
6. **Test Priority :**

   a. Highest

   b. High

   c. Medium

   d. Low
7. **Type Of Testing :**

   a.Positive

   b.Negative
8. **Expected Result**
9. **Actual Result**
10. **Test Result :**

    a.Passed

    b.Failed
11. Test Execution Date : **DD/MM/YYYY**
12. **Remark**

**FLOW PROCESS TESCASE**

![Flow Test Case](https://ik.imagekit.io/kmv5uxk0b/qa_guidance/TESTCASES_FLOW.png?updatedAt=1678775818982 "Flow Test Case")

Information :

1. Create Test Case

   a. Create new test cases

   b. Update test cases
2. Test case Review

   a. Share document testcase

   b. Review with pear team

   c. Review with PM/Developer
3. Update Test Case

   a. Add new test case

   b. Update test case

   c. Priority test case
4. Run Test Case

   a. Run the new test case

   b. Run update test case

**WHAT TEST CASES SHOULD BE EXECUTED DURING THE FEATURE TESTING PERIOD?**

QA should execute Test cases for the new feature and Test Cases regression related to the new feature. Hopefully, with this kind of execution QA can create a better timeline for Feature Testing and reduce testing in Staging Testing Period

*(QA can do E2E Test to ensure new feature run smooth or smoke test or exploratory testing)*

**WHAT IS TEST BED ?**

**Test Bed** is the environment configured for testing. The test bed consists of hardware, software, network configuration, the application being tested, and other related software.

**WHAT IS TEST ENVIRONMENT?**

**Test Environment** is a combination of hardware and software which is where the Tester Team conducts testing.

**Example :**

Application Type: Web Application

OS: Ubuntu

Web Server: LINUX

Web Page Design: React JS

Client-Side Validation: JavaScript

Server-Side Scripting: Node JS

Database: My SQL

Browser: IE/Firefox/Chrome

**WHAT IS TEST DATA ?**

**Test data** is the data used by the tester to run test cases (test cases). When running test cases, the tester needs to enter some input data.

To do this, the tester prepares test data (test data). And can be prepared manually and also by using tools

**WHAT IS TEST CLOSURE?**

Test Closure is a record that is prepared before the test team officially completes the testing process.

This record contains the total number of test cases, the total number of testcases executed, the total number of defects found, the total number of defects fixed, the total number of unfixed bugs, the total number of no rejected bugs, etc.\
\
\
\
All of your pages and images are stored in a top-level directory called **content**, with a sub-folder for your pages (**content/pages**) and one for your images (**content/images**). When you first install your spacebook, it will contain a default welcome page that you can change or delete. 

::: callout
**Did you know?** The trick to managing a spacebook is a basic understanding of Markdown and how it is used to create and organize your content. Use your editor or the Github UI to examine any one of the files in your pages folder to get the lay of the land. 
:::

## Understanding Frontmatter

Frontmatter is a complicated sounding word for a simple concept. Frontmatter is simply a few lines of configuration that live at the top your markdown files. This configuration tells your page what to do and how to behave. The minimal lines of frontmatter for a spacebook page live at the top of the file in between a block of three dashes like so:

```
---
title: Hello world 
date: 2020-11-20
permalink: /hello/index.html
eleventyNavigation:
  order: 10
  key: Hello 
---
```

* **title** -- this is what shows up at the top of your page as the main H1 header
* **date** -- this is the (optional) last updated date that appears at the top of each page. You can use a standard date format such as **2021-01-31**, or the handy **Last Modified** value (which will automatically update each time you save a commit.)
* **permalink** -- the permalink is used to define the URL for the page. It must follow this format, and end with *index.html*
* **eleventyNavigation** -- this is used to define the menu item for your page, and to tell it where it will appear in the menu hierarchy.

  * **order** -- this determines where your menu appears relative to other menu items (0=first) 
  * **key** -- this is the menu "label" for your and also serves a simple slug or key used to track parent and child pages

## Frontmatter options

There are four additional frontmatter items you can add that will affect how your page behaves, including the ability to create a hierarchy of parent and child pages:

```
---
title: About us 
metaDescription: An override for your page's description metatag 👈 
date: 2020-11-20
permalink: /about/index.html
comments: false 👈
eleventyNavigation:
  order: 10
  key: About us 
  parent: Home 👈
  title: A custom menu title 👈
  
---
```

* **metaDescription:** -- this can be used to create a custom description metatag on a page-by-page basis. If not present, the global metatag description from **sites.json** is used
* **comments** -- (opt out) if you have set *enableComments* to true in *site.json* comments will appear on all pages unless you opt out using *comments: false*
* **parent** -- this is used to set up a hierarchy of parent and child pages for your menu system. If you set the *parent* of a given page to match the *key* of another page, it will show up as a child page within the menu system
* **title** -- you add a custom title to change the menu label (useful if you want a short key but a longer menu label)

::: callout
**Did you know?:** If you enable the optional [Netlify CMS integration](/netlifycms), all of these frontmatter settings can be changed via the CMS.
:::

## Adding your content

Once you understand frontmatter, you can begin adding or editing your content using simple markdown. Anything that appears directly below your frontmatter will appear as the main body of your page, like so:

```
---
title: About us 
date: 2020-11-20
permalink: /about/index.html
eleventyNavigation:
  order: 10
  key: About us 
---
This is my content! 👈
```

Your content can include all sorts of [markdown tags](/tips-and-tricks/markdown) and you can organize and structure it however it makes the most sense to you. It is best to use consistent formatting techniques throughout your pages to keep them looking good. 

If you are working locally, you should be seeing all of your changes as you work and if you are editing your Github files directly or using Netlify CMS your changes will appear as soon as the site builds and finishes its deploy. 👍

## Mind your spaces and indents

::: callout
**Mind your spaces!** Be sure to add one space after each entry in your frontmatter and to indent properly, or it will cause an error in your build. The nested options under **eleventyNavigation** are indented with exactly two spaces.