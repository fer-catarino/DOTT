node {
    stage ('Checkout') {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/fer-catarino/DOTT.git']]])
    }
    stage('Static Code Analysis')
    {
    echo "Pa que jale"
    }
    stage('Quality Gate')
    {
    echo "Pa que jale"
    }
    stage('Build')
    {
    echo "ta no"
    }
    stage('Delivery')
    {
    echo "Deliver the code"
    }

}
