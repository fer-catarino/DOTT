node {
    stage ('Checkout') {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/fer-catarino/DOTT.git']]])
    }
    stage('static Code Analysis')
{
echo "Static Code Analysis"
}
stage('Build')
{
echo "Build the code"
}
stage('Unit testing')
{
echo "Unit testing"
}
stage('Delivery')
{
echo "Deliver the code"
}

}
