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
        script {
          echo 'Démarrage des tests...'
          if (fileExists('index.html')) {
            echo "Fichier index.html présent"
          } else {
            error "Fichier index.html manquant"
          }
        }
      }
    }
  }

  post {
    success { echo 'OK ✅' }
    failure { echo 'Échec ❌' }
  }
}
