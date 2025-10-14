## Automated image processing for e-commerce catalog

Template is available as an official n8n workflow at [Enhance Product Photos with Google Gemini AI for E-commerce Catalog](https://n8n.io/workflows/9390-enhance-product-photos-with-google-gemini-ai-for-e-commerce-catalog/). 

### Use cases 
* Monitor a Google Drive folder, process each image based on the prompt defined in `Workflow Configuration` and save the new image to the specified output Google Drive folder.
* Maintain a processing log in Google Sheets.

#### Examples
<table style="border: 0; boder-collapse: collapse; padding: 0;" >
  <tbody>
    <tr>
      <td><img alt="Flower vase" src="assets/flowers.jpg" width=250px  /></td>
      <td><img alt="" src="assets/ai-technology.png" /></td>
      <td><img alt="Fixed Flower vase" src="assets/flowers_clean.png" width=250px  /></td>
    </tr>
    <tr>
      <td><img alt="Mug" src="assets/mug_2.jpg" width=250px  /></td>
      <td><img alt="" src="assets/ai-technology.png" /></td>
      <td><img alt="Fixed Mug" src="assets/mug_2_clean.png" width=250px  /></td>
    </tr>
  </tbody>
</table>

👍 This use case can be extended to any scenario requiring batch image processing, for example, unifying the look and feel of team photos on a company website.


### How it works
* Trigger: Watches a Google Drive folder for new or updated files.
* Downloads the image, processes it using Google Gemini (Nano Banana), and uploads the new image to the specified output folder.


### How to use
* Google Drive and Google Sheets nodes:
  * Create Google credentials with access to Google Drive and Google Sheets. [Read more about Google Credentials](https://docs.n8n.io/integrations/builtin/credentials/google/).
  * Update **all** Google Drive and Google Sheets nodes (6 nodes total) to use these credentials
* Gemini AI node:
  * Create Google Gemini(PaLM) Api credentials. [Read more about Google Gemini(PaLM) credentials](https://docs.n8n.io/integrations/builtin/credentials/googleai/).
  * Update the `Edit Image` node to use the Gemini Api credentials.
* Create a Google Sheets spreadsheet following the steps in `Google Sheets Configuration` (see right ➡️). Ensure the spreadsheet can be accessed as `Editor` by the account used for the Google Credentials.
* Create input and output directories in Google Drive. Ensure these directories are accessible by the account used for the credentials.
* Update the `File Created`, `File Updated` and `Workflow Configuration` node following the steps in the green Notes (see right ➡️).


### Requirements
* Google account with Google API access
* Google AI Studio account with ability to create a Google Gemini API key.
* Basic n8n knowledge: understanding of triggers, expressions, and credential management


### Who’s it for
Anyone wanting to batch process images for product catalog. 
Other use cases are applicable. Please [reach out](https://www.linkedin.com/in/ytkaczyk/) reach out if you need help customizing this workflow. 


### 🔒 Security
All credentials are stored securely using n8n's credential system.
The only potentially sensitive information stored in the workflow is the Google Drive folder and Sheet IDs. These should be secured according to your organization’s needs.


### Need Help?
Reach out on [LinkedIn](https://www.linkedin.com/in/ytkaczyk/) or Ask in the [Forum](https://community.n8n.io/)!



*Attributions*
[Robot icons created by FACH - Flaticon](https://www.flaticon.com/free-icons/robot)

