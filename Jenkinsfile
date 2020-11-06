pipeline {
    agent {
        docker {
            image 'python:3.6'
        }
    }

    stages {
        stage('Install Requirements') {
            steps {
                sh 'pip install -i https://pypi.doubanio.com/simple/ -r ./requirements.txt'
            }
        }
        stage('Style Check') {
            steps {
                sh 'python -m pylint fizzbuzz'
            }
        }
        stage('Test') {
            steps {
                sh 'python -m pytest --cov-branch --cov=fizzbuzz tests/ --cov-report xml:coverage.xml'
            }
        }
        stage('Run') {
            steps {
                echo 'running'
                sh 'python main.py --test-data=./resource/testData.txt'
            }
        }
    }
}