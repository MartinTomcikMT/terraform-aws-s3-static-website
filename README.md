# 🖥️ AWS S3 Static Website



---

## 🎯 Project Goal

The goal of this project was to:

PHASE 1  
* practice basic Terraform workflow
 
PHASE 2  
* improve Terraform project structure

PHASE 3
* serve a custom Cloud/DevOps Knowledge Base webpage through Nginx

PHASE 4
* introduce `terraform.tfvars` for local configuration

---

## ⏱️ Project Status

**Status:** Completed – Phase 4  
**Current Phase:** Phase 4 – Parameterization with tfvars  
**Type:** Infrastructure as Code / DevOps Lab  
**Technologies:** Terraform, Docker, Nginx, WSL, VS Code

---

## ⚙️ Features

* Uses Terraform Docker provider
---

## 🛠️ Technologies Used

* **Terraform** – Infrastructure as Code tool
* **Docker** – Container platform
* **Nginx** – Web server running inside the container
* **WSL** – Linux environment on Windows
* **VS Code** – Code editor
* **Git & GitHub** – Version control and project hosting

---

## 👍 Pre-requisites

To run this project, make sure you have the following installed:

- Terraform
- Docker
- Git
- WSL, if you are working on Windows
- VS Code, optional but recommended

Check installed versions:

```bash
terraform version
docker version
git --version
```

Check if Docker is running:

```bash
docker ps
```

If Docker is running correctly, this command should return a container list, even if the list is empty.

### 💻 Supported environments

- Linux / macOS / Windows
- WSL (Windows Subsystem for Linux)

---

## 🚀 Installation

```bash
git clone https://github.com/MartinTomcikMT/terraform-docker-infra.git
cd terraform-docker-infra
```

---

## ▶️ How to Run

Format Terraform files:

```bash
terraform fmt
```

Initialize Terraform and download the required Docker provider:

```bash
terraform init
```

Validate Terraform configuration:

```bash
terraform validate
```

Preview what Terraform will create:

```bash
terraform plan
```

Apply the configuration and create the Docker container:

```bash
terraform apply
```

Confirm with:

```text
yes
```

After successful deployment, Terraform displays useful outputs:

```text
application_url = "http://localhost:8080"
container_name  = "terraform-nginx"
image_name      = "nginx:latest"

Verify that the container is running:

```bash
docker ps
```

Test the Nginx web server:

```bash
curl http://localhost:8080
```

Or open in browser:

```text
http://localhost:8080
```

Destroy the created infrastructure:

```bash
terraform destroy
```

Confirm with:

```text
yes
```

---

## 🚀 How It Works

1. 

---

## 🧠 What I Learned

PHASE 1  
- how to create a basic Terraform project

PHASE 2  
- how to split Terraform configuration into multiple files

PHASE 3
- how to serve custom content through an Nginx container

PHASE 4
- how Terraform automatically loads values from `terraform.tfvars`

PHASE 5
- how Terraform automatically loads values from `terraform.tfvars`
  
---

## ⚠️ Challenges & Solutions

### Problem:

At first, it was not clear why the Docker container was not visible after pushing the project to GitHub.

### Solution:

I learned that `git push` only uploads the project files to GitHub.  
It does not create infrastructure.

The Docker container is created only after running:

```bash
terraform apply
```

---

### Problem:

Docker command was not available inside WSL.

### Solution:

Docker had to be installed or Docker Desktop WSL integration had to be enabled.  
After Docker was available inside WSL, Terraform could use the Docker provider to create the container.

---



---

## 📸 Screenshots

PHASE 1
<p align="center">
  <table>
    <tr>
      <td align="center">
        <a href="images/terraform-docker-infra_phase1_plan.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase1_plan.jpg" width="400">
        </a><br/>
        <sub>Terraform plan</sub>
      </td>
      <td align="center">
        <a href="images/terraform-docker-infra_phase1_apply.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase1_apply.jpg" width="400">
        </a><br/>
        <sub>Terraform apply</sub>
      </td>
      <td align="center">
        <a href="images/terraform-docker-infra_phase1_docke.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase1_docker.jpg" width="400">
        </a><br/>
        <sub>Running Docker container</sub>
      </td>
      <td align="center">
        <a href="images/terraform-docker-infra_phase1_nginx.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase1_nginx.jpg" width="400">
        </a><br/>
        <sub>Nginx in browser</sub>
      </td>
      <td align="center">
        <a href="images/terraform-docker-infra_phase1_destroy.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase1_destroy.jpg" width="400">
        </a><br/>
        <sub>Terraform destroy</sub>
      </td>
    </tr>
  </table>
</p>
PHASE 2
<p align="center">
  <table>
    <tr>
      <td align="center">
        <a href="images/terraform-docker-infra_phase2_structure.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase2_structure.jpg" width="400">
        </a><br/>
        <sub>Current structure</sub>
      </td>
     <td align="center">
        <a href="images/terraform-docker-infra_phase2_variables.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase2_variables.jpg" width="400">
        </a><br/>
        <sub>Variables file</sub>
      </td>
     <td align="center">
        <a href="images/terraform-docker-infra_phase2_outputs.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase2_outputs.jpg" width="400">
        </a><br/>
        <sub>Outputs file</sub>
      </td>
     <td align="center">
        <a href="images/terraform-docker-infra_phase2_validate.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase2_validate.jpg" width="400">
        </a><br/>
        <sub>Terraform validation</sub>
      </td>
     <td align="center">
        <a href="images/terraform-docker-infra_phase2_plan.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase2_plan.jpg" width="400">
        </a><br/>
        <sub>Terraform plan</sub>
      </td>
     <td align="center">
        <a href="images/terraform-docker-infra_phase2_output.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase2_output.jpg" width="400">
        </a><br/>
        <sub>Output</sub>
      </td>
    </tr>
  </table>
</p>

PHASE 3
<p align="center">
  <table>
    <tr>
      <td align="center">
        <a href="images/terraform-docker-infra_phase3_main.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase3_main.jpg" width="400">
        </a><br/>
        <sub>Main.tf</sub>
      </td>
     <td align="center">
        <a href="images/terraform-docker-infra_phase3_plan.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase3_plan.jpg" width="400">
        </a><br/>
        <sub>Terraform plan</sub>
      </td>
     <td align="center">
        <a href="images/terraform-docker-infra_phase3_apply.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase3_apply.jpg" width="400">
        </a><br/>
        <sub>Terraform apply</sub>
      </td>
     <td align="center">
        <a href="images/terraform-docker-infra_phase3_webpage.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase3_webpage.jpg" width="400">
        </a><br/>
        <sub>Overview of web page</sub>
      </td>
    </tr>
  </table>
</p>

PHASE 4
<p align="center">
  <table>
    <tr>
      <td align="center">
        <a href="images/terraform-docker-infra_phase4_tfvars.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase4_tfvars.jpg" width="400">
        </a><br/>
        <sub>Terraform.tfvars</sub>
      </td>
     <td align="center">
        <a href="images/terraform-docker-infra_phase4_example.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase4_example.jpg" width="400">
        </a><br/>
        <sub>Terraform.tfvars.example</sub>
      </td>
     <td align="center">
        <a href="images/terraform-docker-infra_phase4_plan.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase4_plan.jpg" width="400">
        </a><br/>
        <sub>Terraform plan</sub>
      </td>
     <td align="center">
        <a href="images/terraform-docker-infra_phase4_apply.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase4_apply.jpg" width="400">
        </a><br/>
        <sub>Terraform plan</sub>
      </td>
      <td align="center">
        <a href="images/terraform-docker-infra_phase4_output.jpg" target="_blank">
          <img src="images/terraform-docker-infra_phase4_output.jpg" width="400">
        </a><br/>
        <sub>Output</sub>
      </td>
    </tr>
  </table>
</p>
---

## 📃 Project Structure

```text

```

---

## 📌 Future Improvements

- create reusable Terraform modules

---

## 👤 Author

Martin Tomcik  
Cloud & Infrastructure Engineer | Azure | AWS ☁️
