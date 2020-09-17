# A  Step to Step Guide to Install Anaconda in Ubuntu

In this repository, I am going to guide the following things 
* [How to download and install anaconda](#how-to-download-and-install-anaconda)
* [How to create conda environment and run your code](#how-to-create-conda-environment-and-run-your-code)

## How to download and install Anaconda

### Downlod Anaconda Installer

You can download the Anaconda installer either `Terminal` or `manually from the website`. Follow the following steps to download it manullay from [Anaconda Distribution Page](https://www.anaconda.com/products/individual). 

1. Go to the [Anaconda Distribution Page](https://www.anaconda.com/products/individual#linux) and click `Download`.

   ![2020-09-17](https://user-images.githubusercontent.com/29531232/93409785-43e3e800-f8b5-11ea-83fb-aac7769c7d5b.png)


2. After clicking you will redirect to the various `Anaconda Installer`. Download specific installer for your OS. 

    ![2020-09-17 (1)](https://user-images.githubusercontent.com/29531232/93409870-7db4ee80-f8b5-11ea-860e-c1115ac337a1.png)


3. `Anaconda3-2020.07-Linux-x86_64` will download.

### Install Anaconda

After downloading the installer(`Anaconda3-2020.07-Linux-x86_64`), please make sure where it is located. I put the installer in `Downloads` folder. To install, do following steps

1. Open your `Terminal` and go to the specific folder(in my case, the folder `Downloads`). Then use the following command

   ```sh
   pratik@PRATIK-YOGA:~$ cd Downloads/    
   pratik@PRATIK-YOGA:~/Downloads$ bash Anaconda3-2020.07-Linux-x86_64
   ```
 
2. You will see the following output
 
    ![2020-09-17 (3)](https://user-images.githubusercontent.com/29531232/93409949-a806ac00-f8b5-11ea-9276-dd8e5333580d.png)

3. Click `ENTER` and finally it prompts `yes or no`. Hit enter. It will take a few minutes to install the anaconda.
 
4. The installer prompts `Do you wish the installer to initialize Anaconda3 by running conda init?` Enter `“yes”`.
 
5. **To check if Anaconda install properly, close your terminal and then reopen it. Then type** 
    ```sh
      pratik@PRATIK-YOGA:~$ conda list    
    ```
     It will show a list of packages install through Anaconda. 

## How to create conda environment and run your code

The next step is to create conda environments. To know about the details of the conda environments, you can refer to its [official documentation page](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html). Few basic steps for using the conda environment are follows

### Create conda environment 
Conda environment nothing but a virtual environment. You can customize the environment as per your requirements.
    
1. Suppose, you want to create a conda environment named `first_env`. Use the following command   
  ```sh 
  pratik@PRATIK-YOGA:~$ conda create --name first_env
  ```
    
2. Most in the cases, we need specific version of `Python`. Suppose, you need to install `Python=3.7` and the name of the environment is `second_env`, use the following command 
   ```sh
   pratik@PRATIK-YOGA:~$ conda create --n second_env python=3.7
   ```
   ** __Note, your python version of the conda environment and your local machine can be different.__
    
### Activating the `conda` environment and run your code.
1. You can have multiple `conda` environments. To see all the `conda` environments, use the following command 
    ```sh 
    pratik@PRATIK-YOGA:~$ conda info --envs
    ```
   __Output will be__
    ```sh
    # conda environments:                                                                                                                                                
    #                                                                                                                                                             
    base                  */home/pratik/anaconda3                                                                                                                      
    first_env              /home/pratik/anaconda3/envs/first_env                                                                                                        
    second_env             /home/pratik/anaconda3/envs/second_env   
    ```
    
2. To use any specific `conda` environment, you need to activate it. Suppose, you need to activate `second_env` environment
    ```sh 
    pratik@PRATIK-YOGA:~$ conda activate second_env
    ```
    Now, `second_env` environment is activated. Now you can understand from your terminal only. `pratik@PRATIK-YOGA:~$` will change to `(second_env)pratik@PRATIK-YOGA:~$`
    
3. Now you can run your code in this terminal. For your project, if you need any specific package with specific version, you can install install that following way
* Install specific package: 
