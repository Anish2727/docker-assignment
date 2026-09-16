cat > Jenkinsfile <<'EOF'
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-docker-app:jenkins .'
            }
        }

        stage('Docker Image Check') {
            steps {
                sh 'docker images my-docker-app'
            }
        }
    }
}
EOF
