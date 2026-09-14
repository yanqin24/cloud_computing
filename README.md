---
title: "Assignment 1: Setup Development Accounts"
---
# Assignment 1: Setup Development Accounts

**Points:** 10
**Course:** CSYE 6225 - Network Structures and Cloud Computing, Fall 2026
**Submission Platform:** Gradescope (GitHub-linked autograder)

## Objective

The goal of this assignment is to ensure that every student has set up the necessary accounts and local development environment that will be used for all subsequent Cloud Programming Assignments in this course. Completing these steps is mandatory for success in CSYE 6225.

You will be asked to complete the following tasks:

1. **Account Setup**
   1. Sign up and configure a personal GitHub account (free)
   2. Sign up for the GitHub Student Developer Pack (free)
   3. Get your Assignment 1 repository from the course GitHub organization
   4. Sign up for an AWS Cloud Service account (Paid Plan)
2. **Gradescope Access**
   1. Join the course on Gradescope using the entry code posted in Canvas
3. **Development Environment Setup**
   1. Install git (source code version control software) on your development laptop
      1. Set up your commit email and username in git
   2. Install and set up SSH (Secure Shell, open source software) on your development laptop
      1. Create your public/private SSH keys
      2. Add your SSH keys to GitHub
   3. Install a suitable IDE or text editor on your development laptop

Follow the instructions below on how to submit for credit.

**AI Tools:** allowed for use for document and instruction search. AI attribution will not be required for this assignment.


## Part 0: Accessing Gradescope via Canvas

This course uses Gradescope for all Cloud Programming Assignment submissions. Before doing anything else, join the Gradescope course:

1. Go directly to **[gradescope.com](https://gradescope.com)** in your browser. **Do not access Gradescope through a link embedded inside Canvas** — GitHub's login page will refuse to load inside Canvas's embedded frame, which will block you from linking your GitHub repository later. Always access Gradescope in its own browser tab.
2. Click **Log In**, then choose **School Credentials** and select **Northeastern University** to sign in with your Northeastern account (SSO).
3. If you are not automatically enrolled, click **Add a Course** and enter the **entry code** posted on the Assignment 1 page in Canvas. Ask a TA if you cannot locate the entry code.
4. Once enrolled, you should see **CSYE 6225 - Network Structures and Cloud Computing** on your Gradescope dashboard, along with a listing for Assignment 1.

You only need to complete this join step once for the entire semester — every future Cloud Programming Assignment will already have you enrolled.


## Part 1: Account Setup

In this section, you will create and configure accounts for GitHub and Amazon Web Services (AWS). You may use existing personal accounts if you have them.

### 1.1 GitHub Account

GitHub will be used for version control and for submitting your Cloud Programming Assignments via Gradescope's GitHub-linked autograder.

- **Sign Up:** If you don't already have one, create a free account at <https://github.com/>.
  - **Add your @northeastern.edu email:** Make sure you have your @northeastern.edu email address in your GitHub profile. This helps the teaching staff identify your submissions. If you have an existing account under a different email, you can just add an additional email to your profile.
- **Personalize Your Profile:** To help the teaching staff identify you, please set your public profile to include your full name and a clear profile picture of yourself.
  - Name: Go to Settings > Public profile > Name
  - Picture: Click your profile icon in the top-right and select **Your profile** to upload a picture.
- **GitHub Student Developer Pack:** Sign up for the GitHub Student Developer Pack to get access to free developer tools, including benefits for AWS. Sign up now, as you will be using some of these benefits in later assignments.
  - Apply at: <https://education.github.com/pack>
- **Get Your Assignment 1 Repository:** Your Assignment 1 repository is provided as a template under the course GitHub organization:

  **`https://github.com/neu-csye6225-sea/202609-assignment-01.git`**

  Do **not** clone this URL directly — it is a shared template, and you will not be able to push your own commits to it. Instead:
  1. Open the repository in your browser: <https://github.com/neu-csye6225-sea/202609-assignment-01>
  2. Click the green **Use this template** button, then **Create a new repository**.
  3. Choose your own GitHub account (or the course organization, if you have been given repo-creation access there) as the owner, and give it a name such as `csye6225-assignment-1`.
  4. This creates your own independent copy with a clean history — this is the repository you will work in, commit to, and link to Gradescope.

### 1.2 AWS Account

Amazon Web Services (AWS) will be our cloud platform for this course.

- **Sign Up:** Create an AWS account at <https://aws.amazon.com/>. Select the **Paid Plan** when prompted.
- **Credits for new accounts:** New accounts receive $100 in credits upon sign-up, and can earn up to $100 more by completing onboarding activities, for a maximum of $200. Several of these activities will be covered by later assignments.
- **Unexpected Charges:** You are responsible for monitoring your usage to avoid unexpected charges. It is highly recommended that you set up billing alerts in Cost Explorer.


## Part 2: Local Development Environment Setup

In this section, you will install and configure the core software required for local development.

### 2.1 Install Git

Git is the version control system we will use.

- Download and install Git from <https://git-scm.com/downloads>.
- During installation, accept the default options unless you have a specific reason to change them. (Windows users: the installer also gives you Git Bash, which provides a useful Unix-like command line environment.)

### 2.2 Configure Git

After installation, you must configure Git with your name and email address. These will be attached to every commit you make.

Open your terminal (or Git Bash on Windows) and run the following commands, replacing the placeholder text with your information:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

Use the same name and email associated with your GitHub account.

### 2.3 Configure SSH for GitHub

You will connect to GitHub from your local machine using the SSH protocol for better security.

- **Generate SSH Keys:** If you do not have an SSH key pair (`id_rsa` and `id_rsa.pub`), generate one by following GitHub's official guide: [Generating a new SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).
- **Add SSH Key to GitHub:** Add your public SSH key (the contents of the `id_rsa.pub` file) to your GitHub account by following this guide: [Adding a new SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account).

### 2.4 Install a Code Editor

You will need a text editor for writing code. You are free to choose any editor you prefer for this class. Popular choices include:

- Visual Studio Code
- Sublime Text
- JetBrains IDEs (IntelliJ, PyCharm, etc.)
- Vim


## Part 3: Submission (Gradescope)

Cloud Programming Assignments in this course are submitted and graded through **Gradescope**, using a GitHub-linked autograder. You will submit by connecting your own GitHub repository (created from the template in Part 1.1) to the Gradescope assignment — there is no separate file upload.

If you have not yet joined the course on Gradescope, complete **Part 0** above before continuing.

1. **Clone your own repository** (not the template) to your local machine using the SSH URL:

   ```bash
   git clone git@github.com:<your-github-username>/csye6225-assignment-1.git
   ```

2. **Create a `Submission.txt` file** inside the cloned repository folder.

3. **Add the following information** to your `Submission.txt` file:
   - Your full name
   - Your Northeastern email
   - Your `git config user.name` and `user.email` (run `git config --list` to verify)
   - `github_student_developer_pack: yes`
   - Your AWS account ID
   - `ssh_config: successful` — verify by running `ssh -T git@github.com`. A successful connection returns a message confirming you've authenticated. If you see that message, mark this field `successful`.

   Do **not** include your password or any other sensitive credentials in this file.

   **Example `Submission.txt`:**

   ```text
   assignment: 1
   name: Noah Lott
   email: noah.lott@northeastern.edu
   git_config:
     user.name=nlott
     user.email=noah.lott@northeastern.edu
   github_student_developer_pack: yes
   aws_account_id: 123456789012
   ssh_config: successful
   ```

4. **Commit and push** your `Submission.txt` file to GitHub:

   ```bash
   cd csye6225-assignment-1
   git add Submission.txt
   git commit -m "Complete Assignment 1 setup verification"
   git push origin main
   ```

5. **Link your repository in Gradescope** (first submission only):
   - Log in to Gradescope directly at [gradescope.com](https://gradescope.com) (see Part 0 — do not access it through Canvas).
   - Go to the Assignment 1 entry for CSYE 6225.
   - Click **Submit Assignment** > **GitHub**.
   - If this is your first time, authorize the Gradescope GitHub App to access your account (this works for both public and private repositories).
   - Select your own repository (the copy you created in Part 1.1, e.g. `csye6225-assignment-1`) and the branch `main`.
   - Click **Upload** to submit.

6. **Subsequent submissions:** After the first link, pushing new commits to `main` and resubmitting in Gradescope (or submitting again from the same linked repository) will re-trigger the autograder. You may resubmit as many times as needed before the deadline.

**Grading:** The autograder runs automatically once your submission is received and checks the contents of `Submission.txt`. Your score and detailed feedback appear on the Gradescope assignment page within a few minutes.


## Grading Rubric (10 points total)

- **(2 points)** Name and Northeastern email correctly present in `Submission.txt`.
- **(2 points)** `git config` output (`user.name` and `user.email`) correctly present.
- **(2 points)** SSH connection to GitHub verified (`ssh_config: successful`).
- **(1 point)** Successfully signed up for the GitHub Student Developer Pack.
- **(1 point)** AWS account ID provided.
- **(2 points)** Repository is correctly linked to the Gradescope assignment and the autograder runs successfully.
- **(-3 points)** Sensitive information (e.g., a password) is included in `Submission.txt`.

---

## Appendix: Autograder

This assignment uses a Gradescope autograder linked to your GitHub repository. When you submit, Gradescope pulls the latest commit from your linked branch and runs a script that checks `Submission.txt` for the required fields.

- A successful run shows a score out of 10 directly on the Gradescope assignment page.
- Detailed output for each check is available by expanding the autograder results on your submission page.
- If your submission fails, review the specific failed checks in the Gradescope output, fix the issue in your repository, commit and push, then resubmit in Gradescope.
