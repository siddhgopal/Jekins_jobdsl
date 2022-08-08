job("Job1"){
    description("First job")
    authenticationToken('secret')
    label('dynamic')
    scm {
        github('Asad/jenkins_jobDSL1', 'master')
    }
    triggers {
        gitHubPushTrigger()   
    }
    steps {
        shell ('''
    echo "test"
''')
    }
}
buildPipelineView('project-A') {
    title('Project A CI Pipeline')
    displayedBuilds(5)
    selectedJob('Job1')
    showPipelineParameters()
    refreshFrequency(60)
}