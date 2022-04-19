node {
    stage("Clone code") {
        git https://github.com/modmoios/abcdef.git
    }
    printMessage('Running Pipeline')
    stage("Testing") {
        sh 'python test_functions.py'
    }
    stage("Deployment") {
        if (env.BRANCH_NAME == 'master') {
            printMessage('Deploying the master branch')
        } else {
            printMessage("No deployment for branch [${env.BRANCH_NAME}]")
        }
        
    }
    printMessage('Pipeline Complete')
}

def printMessage(message) {
    echo "${message}"
}
