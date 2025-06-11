# cs-455-cloud-computing-project-1-solved
**TO GET THIS SOLUTION VISIT:** [CS-455-Cloud Computing  Project 1 Solved](https://mantutor.com/product/cs-455-cloud-computing-project-1-solved/)


---

**For Custom/Order Solutions:** **Email:** mantutorcodes@gmail.com  

*We deliver quick, professional, and affordable assignment help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;87487&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS-455-Cloud Computing&nbsp;  Project 1&nbsp;Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Objective

The objectives of Project 1 are:

• &nbsp; &nbsp; &nbsp; Continue practicing using AWS services. &nbsp;In this project you will combine many of the concepts we have looked at to do a simple cloud application (S3, Lambda, RDS, XML, and JSON).

• &nbsp; &nbsp; &nbsp; Learn how S3 Event Notifications work. &nbsp;S3 can publish events to many destinations (including a Lambda function). &nbsp;Read this article about S3 Event Notifications. &nbsp;We also did a module where we configured a Lambda with an S3 trigger (see Module 12).

• &nbsp; &nbsp; &nbsp; Learn how to interact with a relational database running in the cloud.

• &nbsp; &nbsp; &nbsp; Learn how several cloud services can be used together.

Scenario

In the spirit of current events, we will do a scenario related to COVID vaccination. &nbsp;You will devise a system where a central authority (e.g., the Center for Disease Control and Prevention (CDC)) is tasked with keeping track of the vaccination drive taking place across the US. &nbsp;The collected information is useful to monitor areas of the country that are making progress vs. others that are not, adjust policies accordingly, and keep the public informed about the vaccination progress (e.g., by publishing daily numbers in major newspapers).

Let’s start with a few assumptions:

1. &nbsp; &nbsp; &nbsp; The CDC is the central authority that aggregates and keeps track of vaccination data. &nbsp;It does that by collecting daily information that covers the following:

a. &nbsp; &nbsp; &nbsp; Total number of people who have received their first shot.

b. &nbsp; &nbsp; &nbsp; Total number of people who have received their second shot and are considered fully vaccinated.

2. &nbsp; &nbsp; &nbsp; There are thousands of sites across the US administering vaccines (pharmacies, clinics, hospitals, etc.). &nbsp;These sites do not have systems in place to directly communicate with the CDC computer systems. &nbsp;All sites, however, have Internet connections and can upload data to the cloud.

3. &nbsp; &nbsp; &nbsp; The CDC created an AWS S3 bucket and requested all sites to upload at the end of each day a summary of the vaccines administered in each site. &nbsp;The CDC gave sites the option of uploading their data in XML or JSON format. &nbsp;Examples of the expected format are shown in Figure 1.

XML:

JSON:

Figure 1: &nbsp;XML and JSON data examples the CDC is expecting from vaccination sites.

• &nbsp; &nbsp; &nbsp; day, month, year: &nbsp;date of vaccination.

• &nbsp; &nbsp; &nbsp; id: &nbsp;a unique ID the CDC gives each participating site.

• &nbsp; &nbsp; &nbsp; name, zipCode: &nbsp;site name and its location zip code.

• &nbsp; &nbsp; &nbsp; brand: &nbsp;vaccine brand name (assume only two allowed: &nbsp;Pfizer and Moderna).

• &nbsp; &nbsp; &nbsp; total, firstShot, secondShot: &nbsp;total number of people who got a shot at the site in a given day, number that it is their first shot, number that it is their second shot (firstShot + secondShot should be equal to total).

4. Note that not every site administer both vaccine brands. &nbsp;Some sites offer Pfizer only, some offer Moderna only, and some offer both. &nbsp;Therefore, the XML does not necessarily have to have two &lt;brand&gt; elements under &lt;vaccines&gt;. &nbsp;Same applies to the JSON equivalent: &nbsp;the vaccines array may contain only one item.

System Design

Your task is to implement a cloud application for the CDC that works like this:

• &nbsp; &nbsp; &nbsp; At the end of each day, vaccination sites upload their daily summary (in XML or JSON format) to an S3 bucket that the CDC created. &nbsp;Each site uses a simple program (UploadData.exe) to upload the XML or JSON file. &nbsp;The UploadData.exe executable is called from the command line of any computer connected to the Internet. &nbsp;It takes two arguments: &nbsp;The first argument is the path of the file to upload. &nbsp;The second argument is a string (xml or json) that indicates whether the file is XML or JSON. &nbsp;Here are two examples of how UploadData.exe may be called (text in blue is the first argument, and text in red is the second argument):

prompt&gt; &nbsp;UploadData.exe C:\Temp\daily.xml xml

prompt&gt; &nbsp;UploadData.exe C:\vaccination\data\today.json json

UploadData.exe uploads the file passed in the first argument to the S3 bucket and sets with the uploaded object a tag named “type” with a value that indicates if the file is XML or JSON (“xml” or “json”).

• &nbsp; &nbsp; &nbsp; An AWS Lambda function is listening on file arrival to the S3 bucket (using an S3 event notification mechanism). &nbsp;When a file is uploaded to the bucket, S3 triggers the invocation of the Lambda function. &nbsp;Lambda can then read the file content and the “type” tag, parse the file content, extract vaccination data, and enter the data into a PostgreSQL relational database.

• &nbsp; &nbsp; &nbsp; The PostgreSQL relational database schema should have two tables: &nbsp;Sites and Data. &nbsp;Since a given site uploads daily data, you should have a one-to-many relationship between the “Sites” and “Data” tables (use a primary-foreign key combination).

o &nbsp; The Sites table should have the following fields:

SiteID: &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; The site ID (an integer – can be used as the primary key of this table).

Name: &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;A string that represents the site name.

ZipCode: &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; A string that represents the site zip code.

o &nbsp; The Data table should have the following fields:

SiteID: &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;A foreign key (also of type integer) to the Sites’ table SiteID primary key.

Date: &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; The data of vaccination

FirstShot: &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; An integer that represents the first shot.

SecondShot: &nbsp; &nbsp; &nbsp; An integer that represents the second shot.

Note that the SiteID and Date (together) form the primary key of the Data table. &nbsp;That is, the combination of SiteID/Date should be unique.

No need to keep track of vaccine brand. &nbsp;So there is no field for it.

• &nbsp; &nbsp; &nbsp; On any given day, it is possible that a site makes mistakes and need to upload a corrected XML or JSON file. &nbsp;Your system should allow this; in this case a row in the Data table should get UPDATED (not INSERTED since you already have a row for the SiteID/Date combination).

Figure 2 is a diagram that summarizes the workflow of this system.

Figure 2: &nbsp;System workflow

Files to Use for Testing

8 files were provided to you for testing. &nbsp;See folder TestFiles.

Implementation Hints

1. &nbsp; &nbsp; &nbsp; In order to query the S3 objects tags you need privileges beyond what the AWSLambdaExecute policy gives you. &nbsp;To do that, create a custom role and use that role for your Lambda function.

a. &nbsp; &nbsp; &nbsp; Go to the IAM service. &nbsp;Click on Roles. &nbsp;Then click the Create role button.

b. &nbsp; &nbsp; &nbsp; Under Choose a use case, select Lambda then click the Next: Permissions button.

c. &nbsp; &nbsp; &nbsp; Search for the following two policies and check each:

i. &nbsp; &nbsp; &nbsp; &nbsp;AWSLambdaExecute

ii. &nbsp; &nbsp; &nbsp;AmazonS3FullAccess

d. &nbsp; &nbsp; &nbsp; Click the Next:Tags button, then the Next:Review button.

e. &nbsp; &nbsp; &nbsp; Give your role a name (e.g., CDCVaccinationSystemRole).

f. &nbsp; &nbsp; &nbsp; &nbsp;Click the Create role button.

This creates a role named CDCVaccinationSystemRole with two policies attached to it: &nbsp;AWSLambdaExecute and AmazonS3FullAccess.

Now when you use the publish Lambda function wizard in Visual Studio, choose role CDCVaccinationSystemRole for your function (you do this in the second screen – this new role that you created in your account should appear in the dropdown):

2. &nbsp; &nbsp; &nbsp; You need to read the tag “type” associated with the S3 file that was uploaded to S3. &nbsp;Its value will tell you whether the file is of type XML or JSON. &nbsp;You can read the tags associated with an S3 object using a combination of the following classes/methods:

GetObjectTaggingRequest

GetObjectTaggingResponse GetObjectTaggingAsync

This documentation article shows you an example how it is done (expand “Uso dos AWS SDKs” then click the .NET tab). &nbsp;Sorry, I wasn’t able to find the English version of this doc page.

3. &nbsp; &nbsp; &nbsp; To query the PostgreSQL database from the Lambda function, use the Npgsql library. &nbsp;You need to add this package to your Lambda function in Visual Studio.
