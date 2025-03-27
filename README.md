# 🚀 Jenkins Shared Library

## 📌 Overview

This repository contains a **Jenkins Shared Library**, designed to streamline and standardize Jenkins pipeline development. By leveraging this library, teams can **reuse pipeline code**, **enhance maintainability**, and **enforce best practices** across multiple Jenkins projects.

## 🔥 Features

- 📌 **Reusable Pipeline Functions** - Standardized Groovy scripts for Jenkins.
- 🔄 **Modular and Scalable** - Easily extendable for different CI/CD use cases.
- 🔧 **Predefined Stages** - Prebuilt functions for common DevOps tasks.
- 🔑 **Security Best Practices** - Enforces secure coding in pipelines.
- 📜 **Easy Integration** - Works seamlessly with Jenkinsfile.

## 🛠️ Installation

To integrate this shared library into your Jenkins pipeline, follow these steps:

1. **Add the Shared Library in Jenkins**
    - Navigate to **Jenkins Dashboard** → **Manage Jenkins** → **Configure System**.
    - Scroll down to **Global Pipeline Libraries**.
    - Add a new library:
      - **Name:** `jenkins-shared-library`
      - **Source Code Management:** Git
      - **Repository URL:** `https://github.com/mpdhanveer05-prakash/Jenkins-Shared-Library.git`
      - Check `Load implicitly` if you want auto-loading.

2. **Use in Jenkinsfile**

   Add the following in your `Jenkinsfile`:

   ```groovy
   @Library('jenkins-shared-library') _
   pipeline {
       agent any
       stages {
           stage('Build') {
               steps {
                   script {
                       myLibraryFunction()
                   }
               }
           }
       }
   }
   ```

## 🚀 Usage

This library provides several utility functions that can be used within Jenkins pipelines. Example:

```groovy
@Library('jenkins-shared-library') _

def call() {
    pipeline {
        agent any
        stages {
            stage('Checkout') {
                steps {
                    checkout scm
                }
            }
            stage('Build') {
                steps {
                    sh 'mvn clean package'
                }
            }
            stage('Deploy') {
                steps {
                    deployApplication()
                }
            }
        }
    }
}
```

## 🛡️ Security Best Practices

- Always use **credentials binding** to store sensitive information.
- Implement **role-based access control (RBAC)** in Jenkins.
- Regularly update and review **Groovy scripts** for security vulnerabilities.

## 🤝 Contributing

Contributions are welcome! Feel free to fork this repository, make improvements, and submit a pull request.


## 📞 Contact

📧 **Dhanveer Prakash** - [LinkedIn](https://www.linkedin.com/in/mpdhanveer05-prakash/) | [GitHub](https://github.com/mpdhanveer05-prakash)

---

✨ **Happy CI/CD Automation! 🚀**
