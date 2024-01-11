# GPT4V-Image-Captioner / GPT4V图像打标器

[中文版说明]
[英文版说明](https://github.com/jiayev/GPT4V-Image-Captioner/blob/main/README-EN.md)

This is a multifunctional image processing toolbox built with Gradio, capable of labeling images using the GPT-4-vision API or the [cogVLM](https://github.com/THUDM/CogVLM) model. Key features include:

- One-click installation and use
- Single image reverse search and batch labeling
- Choice of cloud-based GPT4 & local CogVLM models
- Visual tag analysis and processing
- Image bucketing for pre-compression
- Keyword filtering and watermark image recognition

Developers: Jiaye, [LEOSAM是只兔狲](https://civitai.com/user/LEOSAM), [SleeeepyZhou](https://space.bilibili.com/360375877), [Fok](https://civitai.com/user/fok3827)，GPT4. Welcome everyone to add more new features to this project.

![下载](https://github.com/jiayev/GPT4V-Image-Captioner/assets/16369810/90612e2b-aac1-4368-84d6-482bb660f5aa)


# Installation and Startup Guide

### Windows (If the automatic installation fails, please refer to the [Manual Installation Instructions](#windows-manual-installation-instructions))

1. Open Command Prompt as administrator and navigate to the directory where you want to clone the repository.
2. Clone the repository using the following command:
    ```
    git clone https://github.com/jiayev/GPT4V-Image-Captioner
    ```
3. Double-click `install_windows.bat` to run and install all necessary dependencies.
4. After the installation is complete, you can launch the GPT4V-Image-Captioner by double-clicking `install_windows.bat`.
5. Hold down Ctrl and click on the URL in the terminal (or copy the URL to your browser), which will open the Gradio app interface in your default browser.
6. Enter the official OpenAI or third-party GPT-4V API Key and API Url at the top of the interface. After setting the image address, you can start tagging the image.

### Linux / macOS

1. Open a terminal and navigate to the directory where you want to clone the repository.
2. Clone the repository using the following command:
    ```
    git clone https://github.com/jiayev/GPT4V-Image-Captioner
    ```
3. Navigate to the cloned directory:
    ```
    cd GPT4V-Image-Captioner
    ```
4. Make the install and start scripts executable with the following command:
    ```
    chmod +x install_linux_mac.sh; chmod +x start_linux_mac.sh
    ```
5. Execute the install script:
    ```
    ./install_linux_mac.sh
    ```
6. Launch the GPT4V-Image-Captioner in the terminal by executing the launch script:
    ```
    ./start_linux_mac.sh
    ```
7. Copy the URL displayed in the terminal and open it in your browser to access the Gradio app interface.
8. Enter the official OpenAI or third-party GPT-4V API Key and API Url at the top of the interface. After setting the image address, you can start tagging the image.


## Change Log

### January 2, 2024
- **One-Click Install & Launch**: Added one-click installation (`install_windows.bat` / `install_linux_mac.sh`) and launch (`Start_windows.bat` / `Start_linux_mac.sh`) features, simplifying the setup and startup process.
- **Environment Setup Instructions**: Supplemented the installation and launch instructions for the program under Windows and Linux environments.

### January 1, 2024
- **Speed Optimization**: Improved the speed of tagging images. Now annotations can be completed within 2-3 seconds.
- **Tag Management**: Provided different handling options for images with existing tags: "Overwrite", "Prepend", "Append", and "Skip".
- **Subfolder Processing**: The new program can now process all image files within folders and subfolders, supporting formats like '.png', '.jpg', '.jpeg', '.webp', '.bmp', '.gif', '.tiff', '.tif'.
- **Interruption Feature**: Added the ability to interrupt the batch tagging process.
- **Error Screening**: Images that fail GPT tagging (e.g., NSFW content) can be moved to a new folder based on keywords.
- **Localization**: Added support for the Chinese language.


### Windows Manual Installation Instructions

1. Open the Command Prompt by pressing `Win + R`, typing `cmd`, and then pressing `Enter`.

2. Clone the repository to your local machine using the following command:
    ```
    git clone https://github.com/jiayev/GPT4V-Image-Captioner
    ```

3. Once cloning is complete, navigate to the cloned directory:
    ```
    cd GPT4V-Image-Captioner
    ```

4. Before installing any dependencies, make sure that Python is installed on your system. Check for Python's presence by typing the following command and pressing `Enter` in the Command Prompt:
    ```
    python --version
    ```
   If Python is not installed, you will get an error message. In that case, please visit the [Python official download page](https://www.python.org/downloads/) and follow the instructions to install it.

5. Create a virtual environment named `myenv` to avoid contaminating the global Python environment:
    ```
    python -m venv myenv
    ```

6. Activate the virtual environment you just created:
    ```
    myenv\Scripts\activate
    ```

7. Update `pip` to date:
    ```
    python -m pip install --upgrade pip
    ```

8. Install the `requests`, `gradio`, and `tqdm` libraries within the virtual environment:
    ```
    pip install scipy networkx wordcloud matplotlib Pillow tqdm gradio requests
    ```

9. After completing the steps above, you can start GPT4V-Image-Captioner by double-clicking the `Start_windows.bat` file.