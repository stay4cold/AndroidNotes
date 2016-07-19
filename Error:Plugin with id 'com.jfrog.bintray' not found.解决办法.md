在上传项目到bintray的时候一直报此错误
Error:Plugin with id 'com.jfrog.bintray' not found.

最后通过查找最终解决，比较低级的错误

需要修改项目的根目录build.gradle文件：

未修改前：

    buildscript {
    repositories {
        jcenter()
    }
    dependencies {
        classpath 'com.android.tools.build:gradle:2.1.2'

        // NOTE: Do not place your application dependencies here; they belong
        // in the individual module build.gradle files
       }
    }

    allprojects {
        repositories {
            jcenter()
        }
    }

修改后：

    buildscript {
        repositories {
            jcenter()
            mavenCentral()
        }
        dependencies {
            classpath 'com.android.tools.build:gradle:2.1.2'
            
            classpath 'com.jfrog.bintray.gradle:gradle-bintray-plugin:1.4'
            classpath 'com.github.dcendents:android-maven-gradle-plugin:1.3'
            // NOTE: Do not place your application dependencies here; they belong
            // in the individual module build.gradle files
        }
    }
    
    allprojects {
        repositories {
            jcenter()
            mavenCentral()
        }
    }

