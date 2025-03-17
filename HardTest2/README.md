# HardTest2 - Setting up R Dev Container in Positron IDE with help of Docker and Devpod

## 🚀 Installing the Required Tools
1. **Install Docker Desktop**  
   - Download and install [Docker Desktop](https://www.docker.com/products/docker-desktop/).

2. **Install DevPod**  
   - Download and install [DevPod](https://devpod.sh/docs/).

3. **Install Positron (IDE for R)**  
   - Download and install [Positron](https://posit.co/download/positron/).

## Creating a Workspace

 1.**Start DevPod and Set Docker as Provider and Positron as IDE** 

 2. **Clone the repo**
    `- git clone https://github.com/r-devel/r-dev-env.git`

 3. **Start your Coding journey in Positron**

## Test

#### Screenshot of the information messages shown when creating the workspace.

![alt text](<Screenshot 2025-03-16 134749.png>)

#### Screenshot of Positron working.

![alt text](image.png)

![alt text](image-1.png)

#### Issues Faced

 1. **Package Installation**
  
  Following message is shown while trying to install a Packages:

   ![alt text](<Screenshot 2025-03-16 161620.png>)

  It is an error due to docker/devpod container and workspace creation. Though it does not cause any problem but this experience can for sure be smoothen.

 2. **Error in Knitting the Rmd File**

 While trying to Knit a Rmd file, File is not Knitted and following message is displayed:

 ![alt text](<Screenshot 2025-03-16 205112.png>)

 ![alt text](<Screenshot 2025-03-16 165953.png>)

 3. **Unable to povide Documentation of a Self Built local Package**

 While trying to run a local package(Package that i built myself), it is able to use different function and even all test passes and everything work perfecly and no error is shown but it is unable to load the documentaion of package.

![alt text](<Screenshot 2025-03-16 170926.png>)

But in R studion it isn't a problem

![alt text](<Screenshot 2025-03-16 170901.png>)

 This is not an issue with other packages available through CRAN/R org but package build locally in system are not able to load Documentation

4. **Error message while trying to Build few Graphs**

Following message is displayed while trying to built few graphs:

 ![alt text](<Screenshot 2025-03-16 162918.png>)

 I am not sure exactly why this message is shown but graph are created with this error message. It might not be so smooth for new users.

#### Experince

During my experience with Positron, I found that while it provides a lightweight and container-friendly environment for R development, it did not quite match the seamless workflow and user experience of RStudio. Several challenges arose, particularly with R Markdown files, where knitting documents did not work. Additionally, there were difficulties in installing and managing packages, which might led to issues. Building R packages within the environment also presented  obstacles that required additional troubleshooting. From a user experience perspective, it has potential, but there are areas where improvements could be enhance such as better error handling and a more intuitive interface. While it serves as a functional alternative, further refinements could make it a more user-friendly tool for R developers.







