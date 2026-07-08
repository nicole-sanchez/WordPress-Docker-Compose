pipeline {
    agent any
    stages {
        stage('1. Descargar código desde GitHub') {
            steps {
                git url: 'https://github.com/nicole-sanchez/WordPress-Docker-Compose.git', branch: 'main'
            }
        }
        stage('2. Detener versiones anteriores') {
            steps {
                bat 'docker compose down'
            }
        }
        stage('3. Levantar WordPress y Base de Datos') {
            steps {
                bat 'docker compose up -d'
            }
        }
        stage('4. Verificar que todo quedó activo') {
            steps {
                bat 'docker ps'
            }
        }
    }
}