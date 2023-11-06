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
    stage('shell') {
            steps {
                echo 'Hello World'
 
                script {
                    def browsers = ['chrome', 'firefox']
                    for (int i = 0; i < browsers.size(); ++i) {
                        echo "Testing the ${browsers[i]} browser"
                    }
                }
            }
    }
}
}
