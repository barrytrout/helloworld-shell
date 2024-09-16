pipeline {
    
    agent any

    parameters {
	booleanParm(name: 'executeTests', defaultValue: True, description: 'Run build tests?')
	booleanParm(name: 'executeDepoy', defaultValue: True, description: 'Deloy build?')
)
    stages {

        stage{"build"} {

	    steps {

		echo "Building apxplication ..."
            }	
	}

	stage("test") {
	    when  {
		expresssion {
		    params.executeTests
	    }
	    steps {
	
		echo "Testing application ..."
	    }
	}

	stage("deploy") {
	    when {
		expression {
		    params.executeDeploy
	    }
	    steps {
	
		echo "Deploying application ..."
	    }
	}
    }
}
