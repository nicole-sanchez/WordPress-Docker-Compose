pipeline {
    agent any
    options { skipDefaultCheckout() }
    stages {
        stage('1. Descargar código desde GitHub') {
            steps {
                dir('C:\\Users\\Nicole\\practica-wordpress') {
                    git url: 'https://github.com/nicole-sanchez/WordPress-Docker-Compose.git', branch: 'main'
                }
            }
        }
        stage('2. Detener servicios anteriores') {
            steps {
                bat '''
cd C:\\Users\\Nicole\\practica-wordpress
docker compose down || exit /b 0
'''
            }
        }
        stage('3. Levantar WordPress y Base de Datos') {
            steps {
                bat '''
cd C:\\Users\\Nicole\\practica-wordpress
docker compose up -d
'''
            }
        }
        stage('4. Verificar estado') {
            steps {
                bat '''
docker ps
'''
            }
        }
    }
}