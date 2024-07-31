import groovy.transform.Field

@Field def utils = null
@Field def utilsInStage = null

node() {
    stage("Prepare") {
        checkout scm
    }

    utils = load("utils.groovy")
    echo "Loaded utils: ${utils}"

    stage("Load libs") {
        utilsInStage = load("utilsInStage.groovy")
        echo "Loaded utils in stage: ${utilsInStage}"
    }

    stage("Test") {
        utils.printInfo("Running tests")
        utilsInStage.printInfo("Running tests")
    }
}
