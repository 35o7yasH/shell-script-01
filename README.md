**🔐** GitHub Repository Read Access Checker
A simple Bash script that lists users who have read (pull) access to a specific GitHub repository using the GitHub API.

📜 Script Info
Author: Yash

Version: v3

Date: 12/07/2025

* Description:
This script helps you identify which users have read (pull) access to a given GitHub repository.

* ⚙️ Prerequisites
Bash shell

curl

jq (used for JSON parsing)

A GitHub personal access token (PAT) with permission to read collaborators

GitHub username and PAT must be stored as environment variables:

bash
Copy
Edit
export username="your_github_username"
export token="your_personal_access_token"
🚀 Usage
bash
Copy
Edit
./read-access-checker.sh <repo_owner> <repo_name>
Example:
bash
Copy
Edit
./read-access-checker.sh octocat Hello-World
This will list all users who have read access to the octocat/Hello-World repository.

🧠 How It Works
The script uses the GitHub REST API to fetch the list of collaborators on the given repo.

It filters and displays only those with pull (read) permission.

If no users with read access are found, it notifies the user.

📌 Notes
This script authenticates using basic auth (username: token).

Ensure your token has at least repo scope for private repos or the appropriate scope for public repos.

🛠️ To Do
Add better error handling for rate limits and invalid tokens

Allow input of credentials via flags or prompts (optional enhancement)

📄 License
MIT License — feel free to modify and use it!

