© The Chancellor, Masters and Scholars of The University of Oxford. All rights reserved.

# Explore different providers

This course is available for multiple cloud providers. Choose your preferred platform:

- [Hello Google Cloud](https://github.com/Oxford-Research-Cloud-Competency-Centre/Hello-gcloud)
- [Hello Microsoft Azure](https://github.com/Oxford-Research-Cloud-Competency-Centre/Hello-azure) (You are here)
- [Hello Amazon Web Services](https://github.com/Oxford-Research-Cloud-Competency-Centre/Hello-aws) (⭐ Most popular)

# Instructions

<details>
<summary>Step 1. Fork (or make a copy of) this repository</summary>

<img width="414" height="370" alt="image" src="https://github.com/user-attachments/assets/6d89a2ee-37ab-4f32-aaa7-b50a79fc222d" />

***
</details>
<details>
<summary>Step 2. Go to the Microsoft Azure front page and type "App Services" in the search bar</summary>

<img width="1257" height="276" alt="image" src="https://github.com/user-attachments/assets/fbc22fe7-d8dc-441c-982b-8f8e56af322c" />

***
</details>
<details>
<summary>Step 3. Go to Create -> Web App</summary>

<img width="929" height="276" alt="image" src="https://github.com/user-attachments/assets/8f188226-bcb0-480a-b7b5-8c8d9341c59b" />

***
</details>
<details>
<summary>Step 4. Create a new resource group for your application</summary>

<img width="745" height="317" alt="image" src="https://github.com/user-attachments/assets/23650a38-4f94-4db8-9172-cae9ab635672" />

***
</details>
<details>
<summary>Step 5. Choose an instance name. Select the latest Python runtime, Linux, and a region (UK South)</summary>

<img width="1045" height="956" alt="image" src="https://github.com/user-attachments/assets/c1da28c8-b9e5-49d1-be83-6877b8c42f30" />

***
</details>
<details>
<summary>Step 6. Go to Deployment, set "Continuous Deployment" to "Enable" and select your repository</summary>

<img width="1071" height="957" alt="image" src="https://github.com/user-attachments/assets/5817dafd-f510-4dbe-a2b9-eec6d9f163b9" />

***
</details>
<details>
<summary>Step 7. You can maintain public access for now (Anyone with the link will be able to access your app).</summary>

<img width="393" height="167" alt="image" src="https://github.com/user-attachments/assets/9c72a5b5-9ac7-4b19-8824-6d2f6621fef7" />

***
</details>
Create the app and wait for deployment. Voilà! Access the URL.

<img width="771" height="381" alt="image" src="https://github.com/user-attachments/assets/cdbb09be-0996-4696-8fdb-af7a819ea79b" />

***

# Going further

<details>
<summary><h2>Modifying the code</h2></summary>

You can commit some changes to your repository and watch how the service is updated automatically. 

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
	 sudo python -m pip install --break-system-packages -r requirements.txt
```

***
</details>
<details>
<summary>Step 4. Run flask</summary>

```	
	 sudo python -m flask run --port=80
```

Open localhost in your browser.   

***
</details>

<img width="280" height="126" alt="image" src="https://github.com/user-attachments/assets/60bc8002-f853-4879-b6d4-b95a35e709d9" />

</details>
