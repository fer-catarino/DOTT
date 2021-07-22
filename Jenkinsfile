node {
    stage ('Checkout') {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/fer-catarino/DOTT.git']]])
    }
    stage('static Code Analysis')
    {
        def scannerhome = tool 'SonarScanner';
        withSonarQubeEnv ('sonarqubeserver')
        sh """${scannerhome}/bin/sonar-scanner \
            -Dsonar.projectKey=SonarQubeServer \
            -Dsonar.exclusion=**README.md \
            -Dsonar.sources=./cidr_convert_api \
            -Dsonar.host.url=http://3.141.27.156:9000 \
            -Dsonar.login=ced03c7762dd1b221eb28e9a5bfa24ad2049a961 """

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
