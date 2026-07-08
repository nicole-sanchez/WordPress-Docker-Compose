pipeline {
    agent any
    
    stages {
        stage('1. Descargar código desde GitHub') {
            steps {
automáticamente
                git url: 'https://github.com/nicole-sanchez/WordPress-Docker-Compose.git', branch: 'main'
            }
        }
        
        stage('2. Detener servicios anteriores') {
            steps {
corriendo, no falle el pipeline.
                sh 'docker compose down || true'
            }
        }
        
        stage('3. Levantar WordPress y Base de Datos') {
            steps {
                sh 'docker compose up -d'
            }
        }
        
        stage('4. Verificar estado') {
            steps {
                sh 'docker ps'
            }
        }
    }
}