# Rlionheart.github.io
website
**Documentation: Setting Up a Jekyll Site on GitHub Pages**

---

### **Overview**
This document outlines the step-by-step process followed to set up a Jekyll-based website and host it on GitHub Pages. It includes essential commands, file paths, and configurations to help retrace the steps or replicate the process.

---

### **1. Prerequisites**
1. Install Ruby:
   - Download Ruby from [RubyInstaller](https://rubyinstaller.org/) (version 3.2.x recommended).
   - Verify installation:
     ```bash
     ruby -v
     ```

2. Install Bundler and Jekyll:
   ```bash
   gem install bundler jekyll
   ```

3. Install Git:
   - Download Git from [git-scm.com](https://git-scm.com/) and set it up.
   - Verify installation:
     ```bash
     git --version
     ```

---

### **2. Create a GitHub Repository**
1. Log into [GitHub](https://github.com/).
2. Create a new repository:
   - For a personal site: Name it `<username>.github.io`.
   - For a project site: Name it anything (e.g., `my-project`).
   - Make it public.

3. Clone the repository locally:
   ```bash
   git clone https://github.com/RLionheart/Rlionheart.github.io.git
   cd Rlionheart.github.io
   ```

---

### **3. Initialize a Jekyll Site**
1. Create the Jekyll site in the cloned repository:
   ```bash
   jekyll new . --force
   ```
   
   **Files Created:**
   - `_config.yml` (configuration settings)
   - `index.markdown` (homepage content)
   - `_posts/` (directory for blog posts)

2. Install dependencies:
   ```bash
   bundle install
   ```

3. Verify the site locally:
   ```bash
   bundle exec jekyll serve
   ```
   Access the local site at:
   ```
   http://127.0.0.1:4000/
   ```

---

### **4. Modify the Jekyll Site**
1. Edit `_config.yml`:
   - Example updates:
     ```yaml
     title: "RLionheart's Site"
     description: "A personal blog hosted on GitHub Pages."
     theme: minima
     ```

2. Customize `index.markdown` for the homepage.

3. Add new blog posts in the `_posts/` directory:
   - File naming format: `YYYY-MM-DD-title.md`
   - Example content:
     ```markdown
     ---
     layout: post
     title: "My First Post"
     ---
     Welcome to my first blog post!
     ```

---

### **5. Push Changes to GitHub**
1. Stage and commit changes:
   ```bash
   git add .
   git commit -m "Initial Jekyll site setup"
   ```

2. Push changes to the repository:
   ```bash
   git push origin main
   ```

---

### **6. Configure GitHub Pages**
1. Go to the repository settings on GitHub.
2. Under **Settings > Pages**, select:
   - **Branch**: `main`.
   - **Directory**: `/ (root)`.
3. Save changes. The site will be available at:
   ```
   https://rlionheart.github.io/
   ```

---

### **7. Troubleshooting and Notes**
1. **Common Errors:**
   - Missing Gems: Add the gem to `Gemfile` and run `bundle install`.
     ```ruby
     gem "logger"
     gem "csv"
     ```

2. **Favicon Issue:**
   - Add a `favicon.ico` file to the root directory to eliminate the `/favicon.ico not found` error.

3. **Custom Domain (Optional):**
   - Purchase a domain and configure DNS records to point to GitHub Pages.

---

### **Key Commands Summary**
- Clone repository: `git clone https://github.com/<username>/<repository>.git`
- Create Jekyll site: `jekyll new . --force`
- Start Jekyll server: `bundle exec jekyll serve`
- Push to GitHub: `git add . && git commit -m "message" && git push origin main`

---

### **Final Output**
Your live site is available at:
[https://rlionheart.github.io/](https://rlionheart.github.io/)

