Overview
========

This guide provides how to use and install Skeepers' GTM template.

Pre-requisites
==============

-   Access to Google Tag Manager: Ensure you have access to your website's GTM account:
-   Site Id: you should have received a site ID from you Skeepers' contact, if you can't find it don't hesitate to ask for it;
-   Data collection endpoint (formed by *swa. +* client domain, the same CNAME you had to create)*.* It will default point to swa.datap.skeepers.io.

Steps to Install Skeepers tracker via GTM
=========================================

We split the installation in different sections, first add a template, than to configure the tags.

Adding a GTM template
---------------------

1.  Access GTM Account

    1.  Sign in to your Google Tag Manager account

2.  Navigate to the Workspace

    1.  Click on the relevant workspace where you want to add the Skeepers tracker

3.  Add a New Tag

    1.  In the workspace, go to "Tags" and click on "New."
    2.  Select "Tag Configuration."

4.  Choose a Tag Type

    1.  Click on "Discover more tag types in the Community Template Gallery."
    2.  Search for "Skeepers" in the Community Template Gallery

5.  Add Skeepers Template

    1.  Click on the Skeepers template to view its details
    2.  Click "Add to Workspace" to add it to your GTM workspace

Adding the tags
---------------

You should add a tag for each of the events you want to track, that means at the end of the configuration you should have 4 tags, **pageview**, **add to cart**, **cart** and **order**. They will share a common configuration, and specific configurations.

1.  Add a Skeepers Tag

    1.  Add the "Site Id" in the required field
    2.  Add the "Endpoint" in the required fied
    3.  Define the event you will add
    4.  Add the necessary information, using available variables or adding new ones as necessary

2.  Trigger Configuration:

    1.  Set the trigger for the tag to fire.

3.  Repeat the process for the different events

4.  Preview and Debug

    1.  Use the "Preview" mode in GTM to test if the Skeepers tag fires correctly on your website.
    2.  Debug any issues that arise during testing before publishing changes.
    3.  To ensure events are being properly uploaded follow the current workflow. Open the developer console, go to the network tab. Filter for "collect?" on the type "Fetch/XHR". You will be able to see what information was sent, our interest will be on the events part. Make sure the event name is correct and the payload have the correspondent fields, it important to notice that extra fields might be present in the payload, they are automatic filled by our SDK and can be ignored.

5.  Save and Submit

    1.  Once the configuration is complete, click "Save" to save the tag configuration.
    2.  After saving, click on "Submit" to publish your changes to GTM.

6.  Publish Changes

    1.  Once you've confirmed that the tag works as expected, click on "Publish" to make the changes live on your website.
