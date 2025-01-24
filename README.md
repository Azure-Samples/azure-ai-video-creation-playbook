# Creating Engaging Videos with Azure AI

This playbook outlines the step-by-step process for creating product videos using AI-driven tools such as Azure AI Speech. Each section includes visual aids and templates to guide you through the workflow.

![Creating Engaging Videos with Azure AI - visual selection dark bg](https://github.com/user-attachments/assets/a322a8c9-87c8-42bb-94fb-c357caefe38c#gh-dark-mode-only)
![Creating Engaging Videos with Azure AI - visual selection light bg](https://github.com/user-attachments/assets/b83f0aa1-873c-41d4-88f8-4d6fe9d57286#gh-light-mode-only)

## Step 1: Script Generation Using ChatGPT

### Objective
Craft precise, engaging video scripts tailored to your audience.

### Process
Open ChatGPT and input specific prompts.
Refine the output based on feedback or additional prompts.

The following is the prompt we used to generate the video scripts for Azure Container Apps:

<details>
<summary>Click to view the prompt</summary>

```
Use the following outline about Azure Container Apps.
Extract the top 5 topics.

Write a 1-minute script for a youtube video, for each of the 5 topics.
Use storytelling to bring it together in a an engaging way.
Start with a question instead of a standard intro, creating a hook and building out context before jumping into main content.

The audience is a highly technical web developer experts and engineers, so use a technical language.

Do not use abreviations. Use terms that are easy to understand for new comers.


Never mention Kubernetes, nor KEDA.

Add short titles for videos.
For each title, add a "- in 1 minute"
Add a description and kewords for each video.

Format the list as follow:
[title]
[script]

For each video, add the following metadata:
- Video Description
- Social Media placeholder
- Social SEO keywords


Here is the full outline:

1. Introduction to Azure Container Apps 
1.1. What are Azure Container Apps? 
1.2. Azure Container Options 
1.3. Azure Container Apps Use Cases 
1.4. Azure Container Apps Organization 
1.4.1. Environments 
1.4.2. Containers 
1.4.3. Revisions   
1.4.4. Secrets 
1.4.5. Ingress 
1.5. Deploying Your First Azure Container App 
1.5.1 Using the Azure Portal 
1.5.2 Using the Azure CLI 
2. Working with Application Lifecycle Management and Revisions 
2.1. Understanding Revisions 
2.2. Change Types 
2.3. Application Lifecycle Management 
2.4. Creating Revisions 
2.5. Blue-Green Deployments 
2.6. Canary Deployments and A/B Testing 
3. Azure Container Apps Networking and Ingress 
3.1. Networking Overview 
3.2. Custom VNETs 
3.3. Understanding Ingress 
3.4. Modifying Ingress Configuration 
4. Microservices and Azure Container Apps 
4.1. What are Microservices? 
4.2. Scaling a Microservice Container App 
4.3. Service Discovery 
5. Microservices and Dapr with Azure Container Apps 
5.1. What is Dapr? 
5.2. Dapr Building Blocks 
5.3. Dapr Components 
5.4. Azure Container Apps and Dapr 
5.5. Enabling Dapr with Azure Container Apps 
5.6. Adding Dapr Components to Azure Container Apps 
5.7. Using Dapr in Services 
6. Azure Container Apps Observability and Continuous Deployment 
6.1. Container Apps Observability 
6.2. Using Log Streaming 
6.3. Using the Container Console 
6.4. Using Azure Monitor 
6.5. Continuous Deployment and Azure Container Apps 
```
    
</details>

## Step 2: Validation by the Product Owner

### Objective
Ensure the script is technically accurate and aligns with product goals.

### Process
1. Share the draft script with stakeholders for review.
2. Gather feedback in a structured format.
3. Revise the script accordingly.

### Visual Aid
Workflow Diagram:

![Creating Engaging Videos with Azure AI - Validation by the Product Owner - light bg](https://github.com/user-attachments/assets/bd3cf06d-15e6-4eaa-a21d-4c6de9e82a22#gh-light-mode-only)
![Creating Engaging Videos with Azure AI - Validation by the Product Owner - dark bg](https://github.com/user-attachments/assets/ced08c57-4906-46a6-a26d-3c36ce6157f8#gh-dark-mode-only)

## Step 3: Voice-Over Creation Using Azure AI

### Objective
Convert the validated script into high-quality speech.

### Process
Test various voice tones and paces to match the video’s purpose.

Fork and clone this repository that contains a ready-to-use script to help you generate your audio files 
- https://github.com/manekinekko/azure-text-to-speech-demo

Follow the instructions to run the script. The generated audio files will be saved under the audio folder.
If you would like to customize the voice, choose a voice from the [catalog](https://ai.azure.com/explore/models/aiservices/Azure-AI-Speech/version/1/registry/azureml-cogsvc/tryout/texttospeech#voicegallery), and then update the environment variables in the `.env` file:

```
SPEECH_VOICE_NAME=
SPEECH_LANGUAGE=
```

> [!IMPORTANT]  
> Make sure the voice model you are using allows customisation.


## Step 4: Avatar Animation and Captioning (optional)

### Objective
Enhance video engagement with animated avatars and captions. This section is optional, you can skip it if you already have the video content available.

> [!NOTE]  
> In the current example we are using Adobe Express but you can use other tools.

### Process: Animate Characters
1. Navigate to https://new.express.adobe.com/home/tools/animate-from-audio
2. Select an avatar style and background that suits the content. 
3. You can optionally adjust the size of your avatar (and drag the avatar in the canvas to position it).
4. We recommend enabling the "Enhance speech" option (but it's optional).
5. Click "browse" to upload the audio file to Adobe Express. The rendering of the animation will begin automatically after you select your file.
6. Download the animation once it's fully rendered (it takes about 40 seconds for a 1-minute audio clip).

![image](https://github.com/user-attachments/assets/31235bb0-b84d-4a49-bce8-16d905d70eb8)

### Process: Add Captions
1. Navigate to https://new.express.adobe.com/home/tools/caption-video
2. Drag and drop or upload the avatar video from previous step.
3. Select the language spoken in the video (English is selected by default).
4. It takes about 30 seconds to generate captions for 1 a minute video.
5. Read carefully the generated captions and fix any typos (especially for technical terms).
6. Choose a style.
7. Download the video with the generated captions.

![image](https://github.com/user-attachments/assets/c09ee49b-b252-417a-8e59-805b89d255cd)

## Step 5: Video Editing

### Objective
Refine videos by adding professional edits and visual assets. 


> [!NOTE]  
> In the current example, we are using Adobe Premiere Pro, but you can use any video editing software.

### Process
1. Import the MP4 video into Adobe Premiere Pro (or use any other video editing software)
2. We recommend the following sequence properties 
  - For YouTube Short (or vertical videos) we recommend a 9:16 format (1080x1920)
  - 44kHz for audio output
3. Enhance the narrative with visuals:
  - You can buy licensed illustrations from https://stock.adobe.com/
  - Or, use diagrams from Microsoft Learn or Docs.
  - Or, use Microsoft PowerPoint (or Apple Keynote) to create your own animated illustrations.
4. Adjust transitions, apply effects, and ensure smooth synchronization.
5. Export the final video in the required resolution and format.

![image](https://github.com/user-attachments/assets/1f9d483f-dd2d-468c-bd8d-0474bd07220c)
![image](https://github.com/user-attachments/assets/ba1db40f-233a-4753-8f1d-c5cbd1e5d18d)

## Final Notes

### Manual Tasks
- Asset integration and narrative illustration require creative input.

### Helpful Links
- https://speech.microsoft.com/
- https://www.adobe.com/express/
- https://helpx.adobe.com/premiere-pro/tutorials.html


