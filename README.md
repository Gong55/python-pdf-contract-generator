# Python Contract Generator 📄✨

A Python automation script that dynamically generates contract documents from an Excel template. This tool was built to streamline internal workflows, reducing the time spent on manual contract creation by an estimated 50-80%. 
It leverages pandas for data handling, python-docx for document templating, and pythainlp for Thai language localization. 

## 🚀 Overview

Manually creating contracts is a repetitive, time-consuming, and error-prone process. This script automates the entire workflow by reading data from a structured Excel file and populating a pre-defined contract template. It was specifically designed for a company's real estate contracts in Thailand, with built-in logic to handle Thai language specifics. 


### Key Features

*   **Data-Driven:** Populates contracts using data from a simple `.xlsx` file.
*   **Template-Based:** Generates documents from a standardized `.docx` template.
*   **Dual Output:** Creates two distinct versions of each contract (e.g., one for the landlord, one for the tenant).
*   **Thai Language Support:** Integrates `pythainlp` for correct Thai language processing and formatting.
*   **Simple to Use:** Designed for non-technical team members with a one-click executable (`.exe`).


## ⚙️ How It Works

The script follows a simple three-step process:
1.  **Read Data**: It uses `pandas` to open `data_input.xlsx` and read the contract details row by row.
2.  **Process Template**: For each row of data, it opens `.docx` templates and dynamically replaces placeholder text with the corresponding data from the Excel file.
3.  **Generate Output**: It saves the populated documents into the `output/` folder, ready for review and printing.

## 📦 Downloads

Due to GitHub's file size limitations, the compiled executable (`contract_maker.exe`) is not stored in this repository. To get the application, follow these steps:

1.  **Download the file** from the link below:
    ➡️ [**Download contract_maker.exe from Google Drive**](YOUR_GOOGLE_DRIVE_LINK_HERE)

2.  **Place the downloaded file** into the main project folder (the same folder that contains `data_input.xlsx`).

**Note:** Your browser or operating system may show a warning when downloading an executable file. This is standard security behavior.


## 🏁 Getting Started

There are two ways to use this application: for end-users and for developers.


### For End-Users (The Easy Way)

1.  **Open `data_input.xlsx`**.
2.  **Fill in the contract details** in the **`Values`** column (Column B). Greyed-out fields are optional.
3.  **Save and close** the Excel file.
4.  **Run `contract_maker.exe`**.
5.  Check the `output/` folder. You will find the generated contract documents inside.


### For Developers

If you want to modify or improve the script, you'll need to run it from the source code.


**Prerequisites:**
*   Python 3.8 or newer
*   pip (Python package installer)


## ⚠️ Limitations & Known Issues

*   **Fixed Template:** The script is currently hard-coded to work with a specific company's contract format. Modifying it for other templates requires changing the source code.
*   **Code Architecture:** As one of my first projects, the script was written in a procedural style. It consists of a long list of functions and lacks an object-oriented design, which can make it difficult to read, maintain, and extend.
*   **Performance:** The current implementation is not optimized for speed and can be slow, especially if you were to adapt it to generate a large number of contracts at once.


## 🗺️ Future Development (Roadmap)

This project was a valuable first version to solve an immediate need. Due to time constraints and other priorities, development is currently on hold. However, here are some planned features for the future:

*   [ ] **Database Integration:** Connect to a database (like PostgreSQL or SQLite) to pull property/client information and log generated contracts.
*   [ ] **User Tracking:** Add functionality to track which team member generated each contract for accountability.
