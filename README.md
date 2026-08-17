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

<img width="452" height="289" alt="image" src="https://github.com/user-attachments/assets/f9efe091-a047-467c-b35f-19565a9b3b7f" />

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
<summary>Go to App Service/Create/Web App. Create a new App Service with default settings, a Basic plan, at least 1 CPU / 1 GB RAM. When prompted, create a new resource group "rg-hello-azure". Select the latest Python runtime (3.14). </summary>

<img width="1005" height="333" alt="image" src="https://github.com/user-attachments/assets/26261a28-92c4-4eaf-a033-bb437369a33c" />

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

You can create your own git repository and set it as the source. Pushing commits to GitHub will now update the app automatically. 

<img width="782" height="381" alt="image" src="https://github.com/user-attachments/assets/4e868748-0d38-4435-acc4-fe522a512476" />

</details>

<details>
<summary><h2>Using a custom domain</h2></summary>

If you want to use a custom domain, go to Settings then Custom Domains in App Services and follow the instructions. If you are not using Azure DNS, you will be asked to create the DNS records in your Cloudflare, Route 53 or other account. 

<img width="516" height="708" alt="image" src="https://github.com/user-attachments/assets/283f23fe-e2a0-44f6-8918-758b6d2fdd4d" />

</details>

<details>
<summary><h2>Cleaning up</h2></summary>

The simplest way to delete all the resources you just created is to type "Resource Groups" in the search bar and delete the group that you created earlier.

![Deleting a service](README_images/resource_group.png)

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
