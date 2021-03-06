---
layout: page
weight: 75
title: Code Editor
navigation:
  show: true
seo:
  title: Code Editor
  override: true
  description:
---

Use the Code Editor to create a template, edit a SendGrid template, or build a campaign with your own custom HTML. With helpful features like preview, tag completion, and error flagging, you can confidently edit your HTML.

* [Getting Started with the Code Editor](#-Getting-Started-with-the-Code-Editor)
* [Uploading Images](#-Uploading-Images)
* [Using Substitution Tags](#-Using-Substitution-Tags)
* [Adding Categories](#-Adding-Categories)
* [Previewing Your Campaign](#-Previewing-Your-Campaign)


{% anchor h2 %}
Getting Started with the Code Editor
{% endanchor h2 %}

1. From the left-hand navigation, select **Marketing**, and then click **Campaigns**. 

1. Click **Create Campaign**.
   <br>To create a campaign from one that has not yet been sent, find the version you want to use and click the **action menu** next to the campaign and then select **Edit** or **Duplicate**. To create a campaign from one that has already been sent, **Duplicate** will be the only option.

   ![]({{root_url}}/images/campaigns_dashboard_categories_search.png)

1. Select the template that you want to use for your campaign.
   <br>You can select a Blank Template, a custom template that you have already created, or one of SendGrid's pre-built templates. For more information, see [Working With Templates](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/templates.html).

1. Select **Code Editor**, and then click **Continue**.
   <br>If you have already built the HTML that you want to use in another application, copy and paste that code directly into the content area of the code editor. You can also write the HTML for your campaign or template directly in the code editor. The code editor has predictive text completion, color-coded syntax highlighting, and detailed error messages.

1. The Code Editor features a **Live Preview** in the content area. The preview will show changes to the HTML as they are made in real time. The default preview mode is in desktop format.
   <br>You can toggle between a preview of how your campaign or template will appear on a recipient's desktop and mobile phone by clicking either the desktop or mobile phone icons above the content area. You can also view a plain-text version of your campaign or template by clicking the **T** icon. When in this preview mode, you can edit the plain text content of your campaign or template by clicking the **Edit Plain Text** button.

{% warning %}
Once you create a new campaign or template in the Code Editor, you cannot switch to the Design Editor.
{% endwarning %}

{% anchor h2 %}
Uploading Images
{% endanchor h2 %}

1. Select the **Images** icon above the HTML code. A window opens where you can upload images to your image library. 

1. Select the image you want from your image library. 

1. Select the **Image Details** tab and copy the URL in the **Image Source URL** tab by clicking **Copy URL**. 

1. Paste this URL in the image source tag in your campaign or template's HTML. For example: `<img src="your image URL here">`

{% anchor h2 %}
Using Substitution Tags
{% endanchor h2 %}

Substitution tags allow you to easily generate dynamic content for each recipient on your contact list. When you send to a list of recipients you can specify substitution tags specific to each recipient.

**To add a substitution tag to your campaign:**

1. Click the **Settings** tab on the left side of the editor.

1. Click the **Tags** tab at the top of the Settings window. 

1. Locate the tag you want to add to your campaign and click it to automatically copy it to your clipboard.

1. Paste the tag into the module.

<table class="table" style="table-layout:fixed">
 <tr>
   <th>Substitution Tag</th>
   <th>Description</th>
   <th>Type</th>
 </tr>
 <tr>
   <td><code>[%email%]</code></td>
   <td>The email address of the recipient</td>
   <td>Personalization</td>
 </tr>
 <tr>
   <td><code>[%first_name%]</code></td>
   <td>The first name of the recipient</td>
   <td>Personalization</td>
 </tr>
 <tr>
   <td><code>[%last_name%]</code></td>
   <td>The last name of the recipient</td>
   <td>Personalization</td>
 </tr>
 <tr>
   <td><code>[Sender_Name]</code>*</td>
   <td>The name of the sender selected when sending your campaign</td>
   <td>Sender Identity</td>
 </tr>
 <tr>
   <td><code>[Sender_City]</code>*</td>
   <td>The city on record for the sender selected when sending your campaign</td>
   <td>Sender Identity</td>
 </tr>
 <tr>
   <td><code>[Sender_State]</code>*</td>
   <td>The state on record for the sender selected when sending your campaign</td>
   <td>Sender Identity</td>
 </tr>
 <tr>
   <td><code>[Sender_Zip]</code>*</td>
   <td>The zip code on record for the sender selected when sending your campaign</td>
   <td>Sender Identity</td>
 </tr>
 <tr>
   <td><code>[Unsubscribe]</code>*</td>
   <td>This tag will be replaced with a link allowing your recipients opt out of any emails you send using the chosen Unsubscribe Group.</td>
   <td>Unsubscribe</td>
 </tr>
 <tr>
   <td><code>[Unsubscribe_Preferences]</code>
   *</td>
   <td>This tag will be replaced with a link allowing your recipients to opt out of any email unsubscribe groups you offer.</td>
   <td>Unsubscribe</td>
 </tr>
 <tr>
   <td><code>[Weblink]</code></td>
   <td>This tag will be replaced with a link allowing your recipients to view your campaign content directly within their web browser.</td>
   <td>Weblink</td>
 </tr>
</table>
*For your convenience, these substitution tags are included by default in the Unsubscribe Module found on the Build tab of the Design Editor. 

For contacts with no entry in a custom field, the substitution tag appears blank. To set a default value, use the following pattern:

`[%first_name | Valued Customer%]`

{% anchor h2 %}
Adding Categories
{% endanchor h2 %}

Assigning categories to a campaign allows you to track emails based on your own categorization system. By assigning your campaign to a category, you can track statistics across multiple similar campaigns. Example categories: "Weekly Digest," "Product Announcements."

1. Click the *Settings* panel located on the left-hand side of the window to expand it.

1. Navigate to the *Settings* tab, and click **Campaign Settings** to expand the menu. 

1. Locate the *Categories* field under *Campaign Settings*.

1. Select the *Add Categories* field and then type in the tag to add and hit enter. 

{% info %}
Currently, only 10 categories can be added to each campaign.
{% endinfo %}

{% anchor h3 %}
Additional Resources
{% endanchor h3 %}

- [A/B Testing](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/a_b_testing.html)
- [Campaign Statistics](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/campaign_stats.html)
- [Design Editor](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/design_editor.html)
