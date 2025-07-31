# UiPath Automation Project

This repository contains the UiPath workflows, assets and configurations for the daily automation exercises of my project. You can run, test using UiPath Studio.

## Table of Contents

- [UiPath Automation Project](#uipath-automation-project)
  - [Table of Contents](#table-of-contents)
  - [Project Overview](#project-overview)
  - [Prerequisites](#prerequisites)
  - [Getting Started](#getting-started)
  - [Folder Structure](#folder-structure)
  - [Branching Strategy](#branching-strategy)
  - [Daily Exercise: Sahibinden Scraping](#daily-exercise-sahibinden-scraping)
  
## Project Overview

This project includes a collection of UiPath workflows demonstrating exercises of each day.

## Prerequisites

* [UiPath Studio](https://www.uipath.com/product/studio) (Community or Enterprise)
* .NET Framework (version required by your UiPath Studio)

## Getting Started

1. **Clone the repository**

   ```bash
   git clone <repo-url>
   cd <repo-name>
   ```

2. **Open in UiPath Studio**

   * Launch UiPath Studio and select **Open Project**
   * Navigate to this folder and open `project.json`

3. **Restore Packages**
   UiPath will automatically restore the NuGet packages when you open the project.

4. **Run a Workflow**

   * In the **Project** panel, expand the `Workflows` folder
   * Double-click any `.xaml` file / most commonly its `main.xaml`
   * Press **Run** to execute

## Folder Structure

```text
├── .gitignore
├── project.json
├── workflows/
│   ├── workflow-1.xaml
│   ├── workflow-2.xaml
│   └── workflow-3.xaml
├── assets/             # input data, sample files
├── tests/              # test workflows & screenshots
└── README.md
```

## Branching Strategy

We use the following Git branching model:

* **dev**: On-development
* **daily/YYYY-MM-DD**: Daily work branches (e.g., `daily/2025-07-29`)
* **hotfix**: Urgent fixes

**Daily workflow**:

1. Checkout `dev` and apply latest changes
2. Create and work on `daily/$(date +%F)` branch
3. Merge your changes daily
4. Commit `daily/YYYY-MM-DD`

## Daily Exercise: Sahibinden Scraping

This automation searches Sahibinden.com for a specified listing, clicks the first matching result, extracts its title, price, and owner information, appends these details to an Excel file (assets/output.xlsx), and then closes the browser.