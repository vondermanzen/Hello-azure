© The Chancellor, Masters and Scholars of The University of Oxford. All rights reserved.

# Explore different providers

This course is available for multiple cloud providers. Choose your preferred platform:

- [Hello Google Cloud](https://github.com/Oxford-Research-Cloud-Competency-Centre/Hello-gcloud)
- [Hello Microsoft Azure](https://github.com/Oxford-Research-Cloud-Competency-Centre/Hello-mazure)
- [Hello Amazon Web Services](https://github.com/Oxford-Research-Cloud-Competency-Centre/Hello-aws) (⭐ Most popular)

# Instructions

<details>
<summary>Step 1. Fork (or make a copy of) this repository</summary>

![Step 2](README_images/download.png)

***
</details>
<details>
<summary>Step 2. Go to the Microsoft Azure front page and type "App Services" in the search bar</summary>

![Step 2](README_images/img1.png)

***
</details>
<details>
<summary>Step 3. Go to Create -> Web App</summary>

![Step 3](README_images/img2.png)

***
</details>
<details>
<summary>Step 4. Create a new resource group for your application</summary>

![Step 4](README_images/img6.png)

***
</details>
<details>
<summary>Step 5. Choose an instance name. Select Python, Linux, and a region (UK South)</summary>

![Step 5](README_images/img3.png)

***
</details>
<details>
<summary>Step 6. Go to Deployment, set "Continuous Deployment" to "Enable" and select your repository</summary>

![Step 6](README_images/img4.png)

***
</details>
<details>
<summary>Step 7. Internet access should already be enabled. Keep it on.</summary>

![Step 7](README_images/img7.png)

***
</details>
Create the app and wait for deployment. Voilà! Access the URL.

![Voilà](README_images/img5.png)

***

# Going further

<details>
<summary><h2>Modifying the code</h2></summary>

You can commit some changes to your repository and watch how the service is updated automatically. 

</details>

<details>
<summary><h2>Using a custom domain</h2></summary>

If you want to use a custom domain, go to Settings then Custom Domains in App Services and follow the instructions. If you are not using Azure DNS, you will be asked to create the DNS records in your Cloudflare, Route 53 or other account. 

![Linking the domain](README_images/custom_domain.png)

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

![API endpoint](README_images/hello_api.png)

</details>

<details>
<summary><h2>User interface</h2></summary>

Missing content

</details>

<details>
<summary><h2>Database writing/reading</h2></summary>

<details>
<summary>Go to the Azure Console and type "SQL" in the search bar</summary>
Missing content
</details>

</details>

<details>
<summary><h2>Storage bucket writing/reading</h2></summary>

<details>
<summary>Go to the Azure Console and type "Storage accounts" in the search bar</summary>
Missing content
</details>

</details>

<details>
<summary><h2>Local testing</h2></summary>

After a while, it's not fun anymore to wait for deployment. You want to test your changes before. 

<details>
<summary>Step 1. Install git and clone the repository on your local machine</summary>

```	
	git clone {repository_link}
```

***
</details>
<details>
<summary>Step 2. Install Python</summary>

```	
https://www.python.org/downloads/
```

***
</details>
<details>
<summary>Step 3. Install dependencies</summary>

```	
	 python -m pip install -r requirements.txt
```

***
</details>
<details>
<summary>Step 4. Run flask</summary>

```	
	 python -m flask run --port=80
```

Open localhost in your browser.   

***
</details>

![Local testing](README_images/local_testing.png)

</details>

<details>
<summary><h2>Running a job on a separate machine</h2></summary>

This web server is not powerful enough to handle sophisticated tasks. What if GPUs are needed for a heavy workflow? Then you need the ability to create machines dynamically and control them remotely (Infrastructure as Code). 

<details>
<summary>Install dependencies</summary>
Missing content
</details>

</details>
