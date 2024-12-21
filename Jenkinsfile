pipeline {
    agent any  // Ejecutará en cualquier nodo disponible

    stages {
        stage('Checkout') {
            steps {
                echo 'Clonando el repositorio...'
                checkout scm
            }
        }

        stage('Building') {
            steps {
                echo 'Building...'
                // Comando de construcción de ejemplo
                sh 'echo "Construcción completada exitosamente"'
            }
        }

        stage('Testing') {
            steps {

                // Verificar si existe un archivo específico
        sh '''
            if [ -f README.md ]; then
                echo "Archivo README.md encontrado."
            else
                echo "Error: Archivo README.md no encontrado." >&2
                exit 1
            fi
        '''

        
                
                
            }
        }

        stage('Deploying') {
            steps {
                echo 'Deploying...'
                // Comando de despliegue de ejemplo
                sh 'echo "Despliegue completado exitosamente"'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finalizado.'
        }
        success {
            echo 'Pipeline completado exitosamente.'
        }
        failure {
            echo 'El pipeline falló.'
        }
    }
}

