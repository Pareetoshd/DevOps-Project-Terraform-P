# DevOps-Project-Terraform-P
Project Overview: The Project that showcases my ability to leverage Infrastructure as Code (Iaac) principles with Terraform to automate and optimize workflows, specifically in a real-world application like Spotify.Terraform will be used to automate the creation and management of these playlists.
Prerequisites: Before we start, make sure you have:-
 	Terraform Installed: Ensure Terraform is installed on your machine. 
 	Docker Installed: Make sure Docker is installed and running.
 	Spotify Account: You need a Spotify account [without premium access]
 	Spotify Developer Account: Register and create an application to get the Client ID and Client Secret.
 	Spotify Provider for Terraform: Install and configure the Spotify provider for Terraform.
 	VS Code Editor: Recommended for editing Terraform files.

## Steps to Complete the Project

### 1. Creating Terraform Code

Start by setting up your Terraform project.

1. Create a new directory for your Terraform project and navigate to it in your terminal.
2. Create a file named `main.tf`.

### 2. Define Provider

In `main.tf`, define the Spotify provider:

![provider](https://github.com/user-attachments/assets/54b9f674-7cee-4711-884d-b797a166bb55)

### 3. Need API Key

To interact with Spotify's API, you need a Client ID and Client Secret.

### 4. Start with App Creation

1. Go to the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/).
2. Log in with your Spotify account.
3. Click on "Create an App".
![spotify dev](https://github.com/user-attachments/assets/b4c548bf-d72b-4456-a9de-a4be18b0cb44)
4.Fill in the required details and create the app.
Name: MYPLAYLIST // Description: Create Spotify playlists using Terraform.
*Redirect URIs: http://localhost:27228/spotify_callback
5.Click on Settings and note down the Client ID and Client Secret. 
![spotify ID](https://github.com/user-attachments/assets/467a357e-49ab-4a40-a3a2-a5fe6e19d532)

### 5. Enter Details

Create a file named `.env` in VS CODE to store your Spotify application's Client ID and Secret:
![TF ID](https://github.com/user-attachments/assets/75024fe5-2ae8-4f2d-a992-f47ddbe6724e)

### 6. Run the Spotify Auth App and Get the API Key

Make sure Docker Desktop is running, and start the authorization proxy server:

docker run --rm -it -p 27228:27228 --env-file ./.env ghcr.io/conradludgate/spotify-auth-proxy
![DOCK](https://github.com/user-attachments/assets/5f4b2cf5-85a1-4b3a-bf4c-7f9853fc469c)

You should get “Authorization Successful” Message , follow the link and agree T/C.

### 8. Continue Creating Terraform Code

Create a file named `.playlist` in VS CODE to store your Spotify application's resources and Tracks:
![spotify TFcode](https://github.com/user-attachments/assets/b9265fb8-5bb3-4c41-aa46-7fc4f821750f)

Create a file named `.terraform.tfvars` in VS CODE to store API Key: [API Key will generate in Step 6]
![api key](https://github.com/user-attachments/assets/d9a25e6c-7c93-4026-9c98-cc00904505c8)
![variablespotify](https://github.com/user-attachments/assets/c315cc99-106b-484f-a613-5977139e4480)

### 9. Initialize and Apply Terraform Configuration

1. Initialize the Terraform configuration:
2. terraform init
3. terraform apply

After applying the Terraform configuration, log in to your Spotify account and verify that the playlists have been created and populated with the specified tracks.

### 11. Verify Playlists on Spotify
![Spotify Playlist](https://github.com/user-attachments/assets/4e60075e-4f47-4b94-bbe4-045666bf9480)


THANKYOUVISITAGAIN❤️





