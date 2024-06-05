pipeline {
    agent any
    
    parameters {
        // Parametre tanımlayın, burada bir örnek parametre veriliyor
        string(name: 'BUILD_TYPE', defaultValue: 'debug', description: 'Enter the build type (debug/release)')
    }
    
    stages {
        stage('Build') {
            steps {
                // İşlem adımları burada olacak
                echo "Building the project with ${params.BUILD_TYPE} configuration"
                // Projenin yapılandırılması, derlenmesi vb. işlemler burada gerçekleşir
            }
        }
        stage('Deploy') {
            steps {
                // Uygulamanın dağıtılması işlemi burada gerçekleşir
                echo "Deploying the project..."
                // Uygulamanın sunuculara dağıtılması işlemleri burada gerçekleşir
            }
        }
        stage('Wait') {
            // Parametrik bekleme süresi
            when {
                expression { params.BUILD_TYPE == 'debug' }
            }
            steps {
                // Debug yapıda bekleme süresi örneği
                script {
                    echo "Waiting for 2 minutes..."
                    sleep time: 120, unit: 'SECONDS'
                }
            }
        }
        stage('Test') {
            steps {
                // Test işlemleri burada gerçekleşir
                echo "Running tests..."
                // Test senaryolarının çalıştırılması burada gerçekleşir
            }
        }
        stage('Deploy to Production') {
            steps {
                // Üretim ortamına dağıtma işlemi burada gerçekleşir
                echo "Deploying to production..."
                // Üretim sunucularına uygulamanın dağıtılması işlemleri burada gerçekleşir
            }
        }
    }
}
