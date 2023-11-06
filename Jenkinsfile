pipeline {
agent any
parameters {
    	choice(name: 'DeployMode', choices:'tag\nbranch', description:'Required: deploy mode')
	string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
}
stages {
    stage('Example') {
        steps {
            echo "Hello ${params.PERSON}"
        }
    }
}
}
