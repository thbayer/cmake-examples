pipeline {
    agent any

    triggers {
        pollSCM ' * * * * * '
    }


    stages {

        stage('Builds') {
            parallel {
/*
            stage('Build - 01-basic/A-hello-cmake') {
                steps {
		            cmakeBuild \
		                installation: 'InSearchPath',
    		            generator: 'Unix Makefiles',
	    	            buildDir: '01-basic/A-hello-cmake/build',
		                sourceDir: '01-basic/A-hello-cmake'
		            
		            sh "cd 01-basic/A-hello-cmake/build; make"
                }
                post {
                    success {
                        sh "01-basic/A-hello-cmake/build/hello_cmake"
                    }
                }
            }


            stage('Build - 01-basic/B-hello-headers') {
                steps {
		            cmakeBuild \
		                installation: 'InSearchPath',
		                generator: 'Unix Makefiles',
    		            buildDir: '01-basic/B-hello-headers/build',
	    	            sourceDir: '01-basic/B-hello-headers'
		            
		            sh "cd 01-basic/B-hello-headers/build; make"
                }
                post {
                    success {
                        sh "01-basic/B-hello-headers/build/hello_headers"
                    }
                }
            }

            stage('Build - 01-basic/C-static-library') {
                steps {
		            sh "cd 01-basic/C-static-library; \
                        cmake -G \"Unix Makefiles\" -S . -B ./build; \
                        cd build; \
                        make"
                }
                post {
                    success {
                        sh "01-basic/C-static-library/build/hello_binary"
                    }
                }
            }

            stage('Build - 01-basic/D-shared-library') {
                steps {
		            sh "cd 01-basic/D-shared-library; \
                        cmake -G \"Unix Makefiles\" -S . -B ./build; \
                        cd build; \
                        make"
                }
                post {
                    success {
                        sh "01-basic/D-shared-library/build/hello_binary"
                    }
                }
            }
*/
            stage('Build - 01-basic/E-installing') {
                steps {
		            sh "cd 01-basic/E-installing; \
                        cmake -G \"Unix Makefiles\" -S . -B ./build; \
                        cd build; \
                        make "
                }
                post {
                    success {
                        sh "01-basic/E-installing/build/cmake_examples_inst_bin"
                    }
                }
            }

            stage('Build - 01-basic/F-build-type') {
                steps {
		            sh "cd 01-basic/F-build-type; \
                        cmake -G \"Unix Makefiles\" -S . -B ./build; \
                        cd build; \
                        make "
                }
                post {
                    success {
                        sh "01-basic/F-build-type/build/cmake_examples_build_type"
                    }
                }
            }


            }
        }
    }
}
