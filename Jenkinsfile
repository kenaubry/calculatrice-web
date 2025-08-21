pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Démarrage du build...'
            }
        }
        stage('Test') {
            steps {
                echo 'Démarrage des tests...'
                powershell '''
                if (Test-Path "index.html") {
                    Write-Output "Fichier index.html présent"
                } else {
                    Write-Error "Fichier index.html manquant"
                    exit 1
                }
                '''
            }
        }
    }
}
