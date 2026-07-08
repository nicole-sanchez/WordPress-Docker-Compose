pipeline {
    agent any
    stages {
        stage('1. Entrar al directorio del proyecto') {
            steps {
                sh 'cd /var/proyecto && ls -la'
            }
        }
        stage('2. Detener servicios anteriores') {
            steps {
                sh 'cd /var/proyecto && docker compose down || true'
            }
        }
        stage('3. Levantar WordPress y Base de Datos') {
            steps {
                sh 'cd /var/proyecto && docker compose up -d'
            }
        }
        stage('4. Verificar que todo quedó activo') {
            steps {
                sh 'cd /var/proyecto && docker ps'
            }
        }
    }
}