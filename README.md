# RepoGuard

## **SecureCode Intelligence Dashboard**

**RepoGuard** is a cybersecurity dashboard that connects to **GitHub repositories**, scans source code for security vulnerabilities, prioritizes risks, and helps teams track remediation.

## **Project Goals**

- **Connect GitHub repositories securely**
- **Detect vulnerable dependencies and outdated packages**
- **Find exposed secrets, API keys, and hardcoded credentials**
- **Identify common code vulnerabilities** such as SQL injection, XSS, and command injection
- **Rank findings** by severity, exploitability, and business impact
- **Assign vulnerabilities** to team members and track their status
- **Provide security reports** and security trends over time

## **Planned Security Tools**

The project may use the following tools:

- **Semgrep** - Static code security analysis
- **Gitleaks** - Exposed secret and credential detection
- **OSV-Scanner** - Open-source dependency vulnerability scanning
- **Trivy** - Container, dependency, and configuration scanning
- **OWASP ZAP** - Dynamic web application security testing
- **Checkov** - Infrastructure-as-code security scanning

The final tools will be selected after the team confirms the **project technology stack**.

## **Planned Features**

### **Repository Integration**

- **GitHub repository connection**
- **OAuth or GitHub App authentication**
- **Repository and branch selection**
- **Manual and scheduled scans**
- **Scan-on-commit functionality**

### **Vulnerability Management**

- **Critical, high, medium, low, and informational severity levels**
- **Vulnerability explanations**
- **Affected files and line numbers**
- **Recommended fixes**
- **Assignment to team members**
- **Due dates and comments**
- **Open, acknowledged, in-progress, resolved, and dismissed statuses**
- **Fix verification scans**
- **Audit history**

### **Dashboard and Reporting**

- **Total vulnerabilities**
- **Critical and high-risk findings**
- **Vulnerabilities by repository and category**
- **Average remediation time**
- **Security score**
- **Security trends over time**
- **Exportable security reports**

## **Planned Architecture**

```text
GitHub Repository
        |
        v
Repository Integration Service
        |
        v
Isolated Scan Worker
        |
        +--> Semgrep
        +--> Gitleaks
        +--> OSV-Scanner
        +--> Trivy
        |
        v
Findings and Risk-Ranking Engine
        |
        v
Database and Web Dashboard
```

## **Security Requirements**

RepoGuard will be designed with **security as a core requirement**.

- **Use least-privilege repository permissions**
- **Encrypt data in transit and at rest**
- **Securely store tokens and application secrets**
- **Use role-based access control**
- **Verify GitHub webhook signatures**
- **Run scans in temporary isolated environments**
- **Restrict scan-worker network access**
- **Apply CPU and memory limits to scan workers**
- **Delete temporary repository data after scanning**
- **Never commit passwords, API keys, or tokens** to the repository

## **Project Structure**

The project structure may change as development continues.

```text
RepoGuard/
├── README.md
├── backend/
├── frontend/
├── scanner/
├── tests/
└── docs/
```

## **Getting Started**

Installation and setup instructions will be added after the team chooses the backend, frontend, and database technologies.

## **Team Workflow**

The `main` branch should contain **stable code**. Team members should create **feature branches** for their work and submit **pull requests** before merging changes.

Example branch names:

```text
feature/github-connection
feature/secret-scanning
feature/dashboard
bugfix/login-error
```

## **Current Status**

This project is currently in the **planning and initial development stage**.

## **License**

This project is currently intended for academic and development purposes.

