node {
    stage ('Checkout') {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/fer-catarino/DOTT.git']]])
    }
    stage('Installing packages') {
            steps {
                script {
                    sh 'pip -r requirements.txt'
                }
            }
        }
    stage('static Code Analysis')
    {
        def scannerhome = tool 'Sonar-Scanner';
        withSonarQubeEnv ('SonarQubeServer')
        sh """${scannerhome}/bin/sonar-scanner \
            -Dsonar.projectKey=SonarQube \
            -Dsonar.exclusion=**/README.md \
            -Dsonar.sources=./cidr_convert_api \
            -Dsonar.host.url=http://3.141.27.156:9000 \
            -Dsonar.login=c1652c5a18a2841bea7cc7ddfa32b420db19e0b9 """

        }
    stage('Quality Gate')
    {
    sh "Pa que jale"
    }
    stage('Build')
    {
    sh "ta no"
    }
    stage('Delivery')
    {
    echo "Deliver the code"
    }

}
