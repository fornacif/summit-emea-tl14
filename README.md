# TL14 - Enhance content creation and diffusion with Adobe Sensei and Adobe Target

## Agenda
[Chapter 01 - Boostrap](#chapter-01---bootstrap)  
[Chapter 02 - Concepts](#chapter-02---concepts)  

## Chapter 01 - Bootstrap

### AEM Start
Start AEM by executing the following steps

1. Open a **Terminal** window and navigate to path */Users/tl14/Desktop/aem-6.5-summit-london*

:computer: `cd /Users/tl14/Desktop/aem-6.5-summit-london`

2. Execute the following command

:computer: `java -Xmx6G -jar cq-quickstart-6.5.0.jar -r author,dynamicmedia_scene7  -nobrowser -nofork`

3. Using Chrome, log in to AEM Author at http://localhost:4502/
* User name: admin
* Password: admin

### Package Installation

1. Download [LAB14 Package](https://github.com/fornacif/summit-emea-tl14/blob/master/package/LAB14-1.0.0-SNAPSHOT.zip?raw=true)
1. Navigate to [CRX/DE](http://localhost:4502/crx/packmgr/index.jsp)
1. Upload Package
<br/>![](screenshots/1.png)
1. Select Package
<br/>![](screenshots/2.png)
1. Install Package
<br/>![](screenshots/3.png)
1. Start Install
<br/>![](screenshots/4.png)

## Chapter 02 - Concepts

During this lab we will work on the [We.Retail](http://localhost:4502/editor.html/content/we-retail/us/en.html) reference site.
We will update the [Equipment](http://localhost:4502/editor.html/content/we-retail/us/en/equipment.html) page and modify some existing components.
For that, we need to gather some Assets that we will use in the Hero banner and some teasers.

:warning: Don't forget to switch to *Preview* mode to activate navigation links.
