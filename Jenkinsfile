node {
    stage ('Checkout') {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/fer-catarino/DOTT.git']]])
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
            -Dsonar.login=3d6038b8e7b0859f7c312c6bdd35d6c9cd04c6b1 """

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
