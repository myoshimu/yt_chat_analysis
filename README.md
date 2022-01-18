# Analyze YouTube Live Chat with Google Cloud
日本語の手順は[こちらのブログ](https://medium.com/google-cloud-jp/yt-live-chat-ab631e81f9c4)を参照ください。<br>
This is a sample code which shows how to use YouTube Live Streaming API and analyze the chat data by Google cloud.
- get_yt_chat.ipynb : Capture the chat data by YouTube Live Streaming API
- chat_analysis.ipynb : Analyze chat data by Google Cloud
- MCzITTAy8G8.csv : Sample data

## Create a Google Cloud Project and Start Vertex AI Workbench instance
1. In the Google Cloud Console, on the project selector page, [select or create a Google Cloud project](https://console.cloud.google.com/projectselector2/home/dashboard?_ga=2.206767764.602316238.1642400036-907245602.1637922374&_gac=1.81231333.1642134288.Cj0KCQiAuP-OBhDqARIsAD4XHpeUL6JJzycmZLXsB9g048QcBAeCs1H5BGyAx8Ol_nhiSou0zPKU188aAv00EALw_wcB). Please see [this help page](https://cloud.google.com/resource-manager/docs/creating-managing-projects) for detailed steps.
2. Make sure that billing is enabled for your Cloud project. [Learn how to confirm that billing is enabled for your project.](https://cloud.google.com/billing/docs/how-to/modify-project#confirm_billing_is_enabled_on_a_project)
3. In the Google Cloud Console, in the Vertex AI section, go to the Workbench page.
4. Open "Managed Notebook" tab and create the new notebook instance(You can leave all settings options as default).
5. After waiting few minutes, "Open JUPYTERLAB" link will appear so please open it. * Authentication needed at the first time

## Copy the sample code at Vertex AI Workbench
1. In the notebook console, open "Git > Clone a Repository" and put this repository url(https://github.com/myoshimu/yt_chat_analysis).
![image](https://user-images.githubusercontent.com/8294746/149869629-b897e4a2-3ed1-45fe-8420-d931d866058b.png)
![image](https://user-images.githubusercontent.com/8294746/149869685-316abb65-900b-406a-affd-0f7c2541e363.png)
2. You will see "yt_chat_analysis" folder at the left side hand so please open it by double click.

## Analyze Live chat data
1. Open "chat_analysis.ipynb" and following notebook will shown at the right hand side.
![image](https://user-images.githubusercontent.com/8294746/149869797-2569e732-8b10-49dd-9193-37e2f31fb02c.png)
2. Notebook consists of code or markup cells. You can execute each cells by clicking the run icon or "Shift+Enter" key.
3. Run all the cells　in order of appearance from the start.<br>
![image](https://user-images.githubusercontent.com/8294746/149869958-f7a7ea33-dbce-4f30-ae36-9270806799e4.png)
<br>If above install section failed with error, please execute `!pip install nlplot -- user` command, too.
4. This code example includes the sample live chat data which is regarding CAPCOM's Monster Hunter.
 ![image](https://user-images.githubusercontent.com/8294746/149870246-6fe056b5-febf-40a2-b09a-8449b56e5a40.png)
5. This data includes sentiment and magnitude score for each comments. Following is visualize image of time series data.
![image](https://user-images.githubusercontent.com/8294746/149870285-ceb08ed6-7a72-474c-889d-55ac46bcf20c.png)
6. Looking at the word cloud, you will see some monster's name which were frequently talked at the Live chat.
![image](https://user-images.githubusercontent.com/8294746/149870417-ea625eb8-8a0e-4502-8093-80aa7e619f49.png)

