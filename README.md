# Data Diggers: The Art of Interacting and Collecting Data from the Web
## Summer 2024 Complexity Global School

Welcome to the *Data Diggers: The Art of Interacting and Collecting Data from the Web* for the 2024 Complexity School repository! This repository contains the Jupyter notebooks for the class. Below you will find instructions to set up the environment, activate and deactivate it, as well as tutorials and resources to help you get started with web scraping using Selenium.

## Table of Contents
- [Installation](#installation)
- [Environment Management](#environment-management)
- [Selenium Tutorial](#selenium-tutorial)
- [Contributing](#contributing)
- [License](#license)

## Installation

Follow these steps to set up the environment for this repository.

### Step 1: Create a Conda Environment
First, create a new Conda environment named `webscraping` with Python 3.11.5:
```bash
conda create -n webscraping python=3.11.5 -c conda-forge
```

### Step 2: Install Required Packages
Next, install the required packages from `requirements.txt`:
```bash
conda install --name webscraping --file requirements.txt
```
#### Package Descriptions
- **pandas==2.2.1**: A data analysis and manipulation library.
- **beautifulsoup4==4.12.2**: A library for parsing HTML and XML documents, useful for web scraping.
- **nb_conda**: Enables Jupyter to recognize and integrate with Conda environments.
- **notebook**: Provides the Jupyter Notebook server and client.
- **lxml**: A library for processing XML and HTML.
- **requests**: A simple HTTP library for making requests to web servers.
- **selenium**: A powerful tool for controlling web browsers through programs and performing browser automation.

### Step 3: Activate the Environment
Activate the `webscraping` environment:
```bash
conda activate webscraping
```

### Step 4: Launch Jupyter Notebook
Start Jupyter Notebook to begin working with the notebooks:
```bash
jupyter notebook
```

### Step 5: Deactivate the Environment
Once you are finished working, deactivate the environment:
```bash
conda deactivate
```

### Final Step: Remove the Environment
If you no longer need the environment, you can remove it:
```bash
conda env remove -n webscraping
```

## Selenium Tutorial

Selenium is a powerful tool for web scraping and browser automation. Below is a brief tutorial to get you started with Selenium.

### Step 1: Install Selenium
Ensure Selenium is installed in your Conda environment (already included in `requirements.txt`).

### Step 2: Download Web Drivers
To control a web browser, Selenium requires a driver. You can download the appropriate driver from [Selenium's official documentation](https://selenium-python.readthedocs.io/installation.html#drivers).

### Example Usage
Here is a basic example of using Selenium with Python:
```python
from selenium import webdriver

# Set up the WebDriver
driver = webdriver.Chrome(executable_path='/path/to/chromedriver')

# Open a website
driver.get('https://www.example.com')

# Interact with the website
element = driver.find_element_by_name('q')
element.send_keys('Complexity School 2024')
element.submit()

# Close the browser
driver.quit()
```
Replace `/path/to/chromedriver` with the actual path to your downloaded ChromeDriver.

For more detailed instructions and examples, refer to the [Selenium documentation](https://selenium-python.readthedocs.io/).

## Contributing

Contributions are welcome! If you have any suggestions, feel free to open an issue or submit a pull request.

## License

This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.


