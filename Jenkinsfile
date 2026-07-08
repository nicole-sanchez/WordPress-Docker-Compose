pipeline {
    agent any
    stages {
        stage('1. Descargar código desde GitHub') {
            steps {
                echo '✅ Repositorio: https://github.com/nicole-sanchez/WordPress-Docker-Compose.git'
                echo '✅ Rama: main'
            }
        }
        stage('2. Detener servicios anteriores') {
            steps {
                echo '🔹 Ejecutar en terminal: docker compose down'
            }
        }
        stage('3. Levantar WordPress y Base de Datos') {
            steps {
                echo '🔹 Ejecutar en terminal: docker compose up -d'
            }
        }
        stage('4. Verificar estado') {
            steps {
                echo '🔹 Ejecutar en terminal: docker ps'
                echo '✅ Pipeline completado correctamente'
            }
        }
    }
}
    
    