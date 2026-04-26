# 🍴 How to Fork Everything (Browser Only)

If you want to own and edit this entire stack—including all the sub-repositories—follow these steps. You can do this entirely in your browser without using the command line.

### 1. Fork the Component Repositories
First, create your own copies of the individual projects. Visit each link and click the **Fork** button at the top right:
* [Fork the Flask Backend](https://github.com)
* [Fork the Pages Frontend](https://github.com)
* [Fork the Spring Backend](https://github.com)

### 2. Fork this Parent Repository
Next, click the **Fork** button at the top of this page ([codespaces-fullstack](https://github.com)).

### 3. Link Your Forks Together
Now you must tell your copy of the parent repository to point to your personal forks instead of the originals.

1.  Navigate to **your fork** of `codespaces-fullstack` on GitHub.
2.  Press the **`.` (period)** key on your keyboard. This opens the GitHub Web Editor.
3.  In the file explorer on the left, click on the `.gitmodules` file.
4.  Update the URLs by replacing `Open-Coding-Society` with your GitHub username:
    ```ini
    [submodule "flask"]
    	path = flask
    	url = https://github.com
    [submodule "pages"]
    	path = pages
    	url = https://github.com
    [submodule "spring"]
    	path = spring
    	url = https://github.com
    ```
5.  Click the **Source Control** icon on the left sidebar (it looks like a branch).
6.  Type a message like `Relink submodules to my forks` and click **Commit and Push**.

### 🚀 Launching your Codespace
1.  Go back to your repository page on GitHub.com.
2.  Click the green **<> Code** button.
3.  Select the **Codespaces** tab and click **Create codespace on main**.
4.  Codespaces will automatically use your updated `.gitmodules` file to pull the code from **your** forks.

---

### 🔑 Troubleshooting Permissions
If your forks are **private**, your Codespace may ask for permission to access them:
*   A pop-up may appear in the bottom right corner of the Codespace asking to **"Authorize"** access. Click **Yes**.
*   If the folders for `flask`, `pages`, or `spring` appear empty, open the terminal in the Codespace and type:  
    `git submodule update --init --recursive`
