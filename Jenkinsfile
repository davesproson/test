pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                retry(3) {
                    sh '[ -d /home/ec2-user/deploy ] || mkdir /home/ec2-user/deploy'
                }

                timeout(time: 3, unit: 'MINUTES') {
                    sh 'cp * /home/ec2-user/deploy'
                }
            }
        }
    }
}
