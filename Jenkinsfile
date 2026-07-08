pipeline {
    agent any
    
    tools {
        dockerTool 'Mydocker' 
    }
    
    stages {
        stage('1. Descargar código desde GitHub') {
            steps {
                git url: 'https://github.com/nicole-sanchez/WordPress-Docker-Compose.git', branch: 'main'
            }
        }
        
        stage('2. Detener servicios anteriores') {
            steps {
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
    
    