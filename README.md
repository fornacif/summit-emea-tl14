# TL14 - Enhance content creation and diffusion with Adobe Sensei and Adobe Target

## Agenda
[Chapter 01 - Boostrap](#chapter-01---bootstrap)  
[Chapter 02 - Overview](#chapter-02---overview)  
[Chapter 03 - Assets](#chapter-03---assets)  
[Chapter 04 - Stock](#chapter-04---stock)  
[Chapter 05 - Fragments](#chapter-05---fragments)  
[Chapter 06 - Personalisation](#chapter-06---personalisation)  

## Chapter 01 - Bootstrap

### AEM Start
Start AEM by executing the following steps

1. Open a **Terminal** window and navigate to path */Users/tl14/Desktop/aem-6.5*

:computer: `cd /Users/tl14/Desktop/aem-6.5-summit-london`

2. Execute the following command

:computer: `java -Xmx4G -jar cq-quickstart-6.5.0.jar -r dynamicmedia_scene7 -nofork`

3. Using Chrome, log in to [AEM Author](http://localhost:4502)
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

## Chapter 02 - Overview

During this lab we will work on the **We.Retail** reference site.
We will update the **Equipment** page and modify some existing components.
For that, we need to gather some Assets that we will use for the Hero Banner and Teasers.

1. Navigate to [AEM Home Page](http://localhost:4502/aem/start.html)
1. Open the [Sites](http://localhost:4502/sites.html/content) module
<br/>![](screenshots/5.png)
1. Open the [Equipment](http://localhost:4502/editor.html/content/we-retail/us/en/equipment.html) page in edition mode
<br/>![](screenshots/6.png)
1. Observe page structure
<br/>![](screenshots/7.png)

:bulb: Note that components are not editable, they inherit from the master page. Later, we will cancel inheritance of components we want to update.

:warning: Don't forget to switch from *Edit* to *Preview* mode to activate navigation links.

## Chapter 03 - Assets

### Assets Upload

1. Navigate to [AEM Home Page](http://localhost:4502/aem/start.html)
1. Open the [Assets](http://localhost:4502/assets.html/content) module
<br/>![](screenshots/8.png)
1. Open the [Summit EMEA 2019](http://localhost:4502/assets.html/content) folder
<br/>![](screenshots/9.png)
1. Download the three following images
	* [AdobeStock_127970082.jpeg](https://raw.githubusercontent.com/fornacif/summit-emea-tl14/master/images/AdobeStock_127970082.jpeg)
	* [AdobeStock_105076852.jpeg](https://raw.githubusercontent.com/fornacif/summit-emea-tl14/master/images/AdobeStock_105076852.jpeg)
	* [AdobeStock_186488201.jpeg](https://raw.githubusercontent.com/fornacif/summit-emea-tl14/master/images/AdobeStock_186488201.jpeg)
1. Rename images by adding your initials to them
<br/>:warning: `AdobeStock_127970082-FFO.jpeg`
1. Upload theses images through Drag & Drop
<br/>![](screenshots/10.png)
1. Open assets properties
<br/>![](screenshots/11.png)
1. Observe automatically added tags add through **Smart Tags** feature
<br/>![](screenshots/12.png)
1. Open **Smart Crop** editor for each assets
<br/>![](screenshots/13.png)
1. Observe which parts of images have been selected for both *TEASER* and *HERO* formats. 
<br/>![](screenshots/14.png)
<br/>:bulb: The configuration of Smart Crop formats has been made [here](http://localhost:4502/mnt/overlay/dam/gui/content/processingprofilepage/imageprocessingprofiles/editor.html/conf/global/settings/dam/adminui-extension/imageprofile/smart-crop) and the image profile has been applied to the DAM folder.
	
### Assets Usage

1. Navigate to [AEM Home Page](http://localhost:4502/aem/start.html)
1. Open the [Sites](http://localhost:4502/sites.html/content) module
1. Open the [Equipment](http://localhost:4502/editor.html/content/we-retail/us/en/equipment.html) page in edition mode

#### Teaser Update

1. Cancel inheritance of the top left Teaser
<br/>![](screenshots/15.png)
1. Search for Assets by term "**hiking**"
<br/>![](screenshots/16.png)
1. Here we can filter images to refine results. That's where Smart Tags feature is powerful. If we want only images for summer campaign, we can search "**hiking summer**" to have more appropriate results. 
<br/>:bulb: Keep in mind tags are coming from the file itself or enriched by Smart Tags features and thus have not been edited manually
<br/>![](screenshots/17.png)
1. Drag & Drop the first image (the one previously upload) to the top left Teaser
<br/>![](screenshots/18.png)
<br/>:bulb: Note that the image as been cropped accordingly thanks to the **Smart Crop** feature.

#### Hero Banner Update

1. Cancel inheritance of the Hero Banner
<br/>![](screenshots/19.png)
1. Search for Assets by term "**biking**"
<br/>![](screenshots/20.png)
1. Drag & Drop the first image (the one previously upload) to the Hero Banner
<br/>![](screenshots/21.png)
<br/>:bulb: Note that the image as been cropped thanks to the **Smart Crop** feature. Here the focus is made on the cyclist which is not necessary what we want
1. Open Smart Crop configuration for the cycling image and adapt it do focus on bike as we want to highlight equipments. Save changes.
<br/>![](screenshots/22.png)
1. Refresh the Equipments page to see results
<br/>![](screenshots/23.png)
1. Cancel inheritance of the bottom left Teaser
<br/>![](screenshots/24.png)
1. Drag & Drop the biking image to the bottom left Teaser
<br/>![](screenshots/25.png)
<br/>:bulb: Note that the image as been cropped differently from the Hero Banner as it's using another format even if it's the same original image.

## Chapter 04 - Stock

Now we want to find inspiration in **Adobe Stock** catalog to find more relevant visuals.

#### Teaser Update

1. Navigate to *Assets* module root and click on **Search Adobe Stock** icon
<br/>![](screenshots/26.png)
1. Search for Assets by term "**biking**"
<br/>![](screenshots/27.png)
1. Save the already licensed image
<br/>![](screenshots/28.png)
<br/>:warning: License feature as been disabled on purpose as it needs proper account with credits
1. Proceed to Next
<br/>![](screenshots/29.png)
1. Select *Summit EMEA 2019* folder
<br/>![](screenshots/30.png)
1. Go back to the *Equipment* page, search last **biking** images and Drag & Drop it to the biking Teaser
<br/>![](screenshots/31.png)
1. Do the same steps for replacing the *RUNNING* Teaser by an image coming from Adobe Stock
<br/>![](screenshots/32.png)
1. Then
<br/>![](screenshots/33.png)
1. Then
<br/>![](screenshots/34.png)

## Chapter 05 - Fragments

Now we want to create variations of the previously modified content. To do so we will leverage Experience Fragment.

### Experience Fragment Creation

1. Navigate to the [Equipment](http://localhost:4502/editor.html/content/we-retail/us/en/equipment.html) page
1. Convert Teaser to **Experience Fragment Variation**
<br/>![](screenshots/35.png)
1. Set properties for the Experience Fragment to *Summit EMEA 2019*. Choose an appropriate name that contains your initials like:
`Hiking XP Master - FFO`
<br/>![](screenshots/36.png)
1. Select destination for the Experience Fragment to *Summit EMEA 2019*
<br/>![](screenshots/37.png)
1. Select template for the Experience Fragment
<br/>![](screenshots/38.png)
1. Once the Teaser has been converted to Experience Fragment, edit it
<br/>![](screenshots/39.png)
1. Create two variation as live copy
<br/>![](screenshots/40.png)
1. Name must contain the variation name and your initials
<br/>![](screenshots/41.png)
1. Cancel inheritance for new Experience Fragments and replace images by ones coming from Adobe Stock. You can use the search by similarity. Be creative :blush:
<br/>![](screenshots/42.png)
1. Preview newly created Experience Fragments
<br/>![](screenshots/43.png)

### Experience Fragment Export to Target

1. Navigate the [Experience Fragements](http://localhost:4502/aem/experience-fragments.html/content/experience-fragments) module
<br/>![](screenshots/44.png)
1. Switch view to *List View* mode
1. Select all Experience Fragments and export them to Target
<br/>![](screenshots/45.png)
1. As you don't have a Publish instance, just click *Export without Publishing*
<br/>![](screenshots/46.png)

## Chapter 06 - Personalisation

Now we created personalised content, we can build A/B Testing, Automated Personalisation or Experience Targeting activities in Adobe Target.

The following steps will be showed during the lab and we will integrate your previously created Experience Fragments to see the result on the shared AEM Publish instance.

1. A/B Testing activity creation
<br/>![](screenshots/47.png)
1. Publish instance URL selection
<br/>![](screenshots/48.png)
1. Replacement of Experience B by Experience Fragment exported from AEM
<br/>![](screenshots/49.png)
1. Selection of the corresponding Target Offer
<br/>![](screenshots/50.png)
1. Experience B Preview
<br/>![](screenshots/51.png)
1. Experience C Preview
<br/>![](screenshots/52.png)
1. A/B Testing activity overview
<br/>![](screenshots/53.png)