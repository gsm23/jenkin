#!groovy

// Orig Ref From :: https://github.com/loverde/jenkinsfile-test/blob/master/Jenkinsfile



stage name: 'setup'
node {
    if (isUnix()) {
        echo "unix mode"
	    sh 'pwd'
        sh "ls -la"
    } else {
        echo "windows mode"
        bat "pwd"
        bat "dir"
    }
/*
    wrap([$class: 'Groovy']) {
        def script = '''
        println "\n\nSystem Properties"
        System.properties.each { k,v -> println "$k = $v" }
        println "\n\nEnvironment"
        System.getenv().each { k,v -> println "$k = $v" }
'''
    }
*/

    // Testing
    git url: 'https://github.com/gsm23/python_projects'
}

stage name: 'build'
node {
    if (isUnix()) {
         sh 'uname -a'
		 sh 'sleep 5'
    } else {
        bat 'echo NonLinux'
    }
}

stage name: 'postbuild'
node {
    if (isUnix()) {
        sh 'ls -la'
    } else { 
        bat 'dir'
    }
}