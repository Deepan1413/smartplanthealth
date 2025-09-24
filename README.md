# smart_plant_health


A new Flutter project.
while running this project you may notice some package error . to solve it change this package content
C:\Users\seera\AppData\Local\Pub\Cache\hosted\pub.dev\tflite_v2-1.0.0\android\build.gradle

"build.gradle"


group 'sq.flutter.tflite'
version '1.0-SNAPSHOT'

apply plugin: 'com.android.library'
apply plugin: 'kotlin-android' // if needed

android {
    namespace 'sq.flutter.tflite'  // MUST match AndroidManifest.xml package
    compileSdk 35

    defaultConfig {
        minSdk 21
        targetSdk 35
        testInstrumentationRunner 'androidx.test.runner.AndroidJUnitRunner'
    }

    lint {
        disable 'InvalidPackage'
    }

    buildTypes {
        release {
            minifyEnabled false
        }
    }
}

repositories {
    google()
    mavenCentral()
}

dependencies {
    implementation 'org.tensorflow:tensorflow-lite:2.14.0' // or latest stable
    implementation 'org.tensorflow:tensorflow-lite-gpu:2.14.0'
}

