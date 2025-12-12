# Taskflow
🚀 Features

Collaborative development of Postman collections

Version control using Git & GitHub

Automatic synchronization of exported Postman collections

Pull Request workflow for reviewing API updates

Supports multiple environments (e.g., dev, staging, prod)

Clear folder structure for organized API management

📂 Project Structure
taskflow/
├── collections/
│   ├── TaskFlow.postman_collection.json
│   └── ...
├── environments/
│   ├── dev.postman_environment.json
│   ├── staging.postman_environment.json
│   └── ...
├── scripts/
│   └── export.sh  (optional automated exporter)
└── README.md

🛠️ How It Works

Team members build and update APIs in Postman.

Collections are exported from Postman.

Exported collections/environments are added to the repo under collections/ and environments/.

Changes are pushed via Pull Requests for review.

GitHub maintains full history, making changes traceable and reversible.

📥 How to Contribute

Clone this repository

git clone https://github.com/deeksha-1234-acc/Taskflow.git
cd taskflow


Create a new branch

git checkout -b feature/update-collection


Export your updated Postman collection

In Postman:
Collections → “…” menu → Export → 2.1 format

Replace the file in:

collections/taskflow.postman_collection.json


(or add a new collection)

Commit your changes

git add .
git commit -m "Updated TaskFlow API collection"


Push and create a PR

git push origin feature/update-collection

🤖 Optional: Automated Export Script

You can automate exporting via the Postman CLI (Newman):

npm install -g newman


Example script (scripts/export.sh):

#!/bin/bash
newman collection export <COLLECTION_ID> \
  --output ./collections/TaskFlow.postman_collection.json


Run via:

./scripts/export.sh

📌 Best Practices

Always include meaningful commit messages.

Export collections using v2.1 format.

Follow naming conventions for collections and environments.

Use PRs for all changes—avoid pushing directly to main.

Add documentation when introducing new API endpoints.

📄 License

This project is licensed under the MIT License.
Feel free to use, modify, and adapt it to your workflow.
