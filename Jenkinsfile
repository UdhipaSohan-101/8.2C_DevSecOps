pipeline {
  agent any
  stages {
    stage('Build') {
      steps { echo 'Task: Compile & package code | Tool: Maven' }
    }
    stage('Unit & Integration Tests') {
      steps { echo 'Task: Run unit & integration tests | Tools: JUnit (unit), Newman/Postman (integration)' }
    }
    stage('Code Analysis') {
      steps { echo 'Task: Static code analysis | Tool: SonarCloud/SonarScanner (or ESLint for JS)' }
    }
    stage('Security Scan') {
      steps { echo 'Task: Dependency & vuln scan | Tool: OWASP Dependency-Check (or npm audit for Node)' }
    }
    stage('Deploy to Staging') {
      steps { echo 'Task: Deploy artifact to staging (e.g., EC2) | Tool: Ansible' }
    }
    stage('Integration Tests on Staging') {
      steps { echo 'Task: Run end-to-end tests on staging | Tool: Cypress' }
    }
    stage('Deploy to Production') {
      steps { echo 'Task: Deploy to production (controlled) | Tool: Ansible' }
    }
  }
}