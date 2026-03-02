pipeline { 

    agent any 

 

    stages { 

        // СТАДИЯ 1: Получение кода 

        stage('Checkout Code') { 

            steps { 

                echo 'Забираем код из GitHub...' 

                checkout scm 

            } 

        } 

         

        // СТАДИЯ 2: Проверка файлов 

        stage('Check Files') { 

            steps { 

                echo '📄 Проверяем созданные файлы...' 

                sh ''' 

                    echo "=== ФАЙЛЫ В РЕПОЗИТОРИИ ===" 

                    ls -la 

                    echo "" 

                    echo "=== ПРОВЕРКА НАШИХ ФАЙЛОВ ===" 

                    if [ -f Dockerfile ]; then 

                        echo "Dockerfile найден" 

                        echo "Содержимое Dockerfile:" 

                        head -10 Dockerfile 

                    else 

                        echo "Dockerfile не найден" 

                    fi 

                     

                    if [ -f requirements.txt ]; then 

                        echo "requirements.txt найден" 

                    else 

                        echo "requirements.txt не найден" 

                    fi 

                     
    } 

} 
