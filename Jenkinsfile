
pipeline {
    agent none

    stages {
        stage('Build Assets') {
            agent any

            steps {
                echo 'Building Assets...123'
		sh 'python -m py_compile sources/add2vals.py sources/calc.py'
		sh 'cp -r ~/.jenkins/workspace/simple-python-pyinstaller-app/sources/ build'
            }
        }
        stage('Test') {
            agent any

            steps {
                echo 'Testing stuff...'
            }
        }
    }
}
