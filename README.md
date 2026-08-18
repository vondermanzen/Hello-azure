© The Chancellor, Masters and Scholars of The University of Oxford. All rights reserved.

# Explore different providers

This course is available for multiple cloud providers. Choose your preferred platform:

- [Hello Google Cloud](https://github.com/Oxford-Research-Cloud-Competency-Centre/Hello-gcloud)
- [Hello Microsoft Azure](https://github.com/Oxford-Research-Cloud-Competency-Centre/Hello-azure) (You are here)
- [Hello Amazon Web Services](https://github.com/Oxford-Research-Cloud-Competency-Centre/Hello-aws) (⭐ Most popular)

# Instructions

<details>
<summary>Clone this repository (Optional: fork it)</summary>

```bash
git clone https://github.com/Oxford-Research-Cloud-Competency-Centre/Hello-azure.git
```

<img width="409" height="255" alt="image" src="https://github.com/user-attachments/assets/31ebd845-6692-43b9-ba98-125425bc0287" />

***
</details>

<details>
<summary>Zip the repository</summary>

```bash
git archive --format=zip --output=output.zip HEAD
```

***
</details>

<details>
<summary>Go to App Service/Create/Web App. Create a new App Service titled "hello-azure" with default settings, a Basic B1 plan (at least 1 VCPU / 1 GB RAM). When prompted, create a new resource group "rg-hello-azure". Select the latest Python runtime (3.14). </summary>

<img width="1002" height="332" alt="image" src="https://github.com/user-attachments/assets/0c98e83c-4e24-4950-b583-bb1023ad9d8a" />

***
</details>

<details>
<summary>Go to Deployment/Deployment Center/Manual Deployment and upload the zip file that you created earlier</summary>

<img width="1510" height="498" alt="image" src="https://github.com/user-attachments/assets/c3258534-d62b-458d-a489-2677fdc1e6be" />

***
</details>

The app should now be publicly accessible. 

<img width="586" height="298" alt="image" src="https://github.com/user-attachments/assets/ad0f9d95-a693-4a2a-86d9-d6282c0850b1" />

***

# Going further

<details>
<summary><h2>Zipping changes</h2></summary>

The previous command will only zip committed changes. Change the command to be able to include uncommitted changes. 

```bash
zip -r output.zip . -x ".git/*"
```

</details>

<details>
<summary><h2>Continuous deployment</h2></summary>

You can create your own git repository and set it as the source in Deployment/Deployment Center. Pushing commits to GitHub will now update the app automatically. 

<img width="782" height="381" alt="image" src="https://github.com/user-attachments/assets/4e868748-0d38-4435-acc4-fe522a512476" />

</details>

<details>
<summary><h2>Using a custom domain</h2></summary>

In Settings/Custom Domains you can setup a custom domain with SSL certificates. If your domain wasn't purchased in Azure, instructions are provided to setup DNS records externally (Cloudflare, Route 53).

<img width="581" height="553" alt="image" src="https://github.com/user-attachments/assets/a174c3af-c74f-4255-93c4-ee178ae14696" />

</details>

<details>
<summary><h2>Cleaning up</h2></summary>

The service has a delete button. However, it is possible that other resources have been created. Therfore, deleting the entire resource group is usually safer. 

<img width="671" height="160" alt="image" src="https://github.com/user-attachments/assets/6feb4d63-0d1d-47e0-a5d4-130fa9011690" />

</details>

<details>
<summary><h2>Adding an API endpoint</h2></summary>

Add the following code in app.py

```	
@app.route("/hello_api")
def hello_api():
    return {
		"name": "Wrinkle Five Star",
		"species": "Duck",
		"breed": "American Pekin",
		"hatching_date": "2020-09-09",
		"sex": "Male"
    }
```

Then test your endpoint

<img width="638" height="220" alt="image" src="https://github.com/user-attachments/assets/137cd727-30c0-4ee7-bbfd-63f29d16e2b3" />

</details>

<details>
<summary><h2>Local testing</h2></summary>

You need to test your changes before publishing them. 

<details>
<summary>Install Python</summary>

```	
https://www.python.org/downloads/
```

***
</details>
<details>
<summary>Install dependencies</summary>

```	
python -m pip install --break-system-packages -r requirements.txt
```

***
</details>
<details>
<summary>Run flask</summary>

```	
python -m flask run --port=80
```

Open localhost in your browser.   

***
</details>

<img width="280" height="126" alt="image" src="https://github.com/user-attachments/assets/60bc8002-f853-4879-b6d4-b95a35e709d9" />

</details>
