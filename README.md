# AgentsPartner

# Realm

Reference: https://realm.io/docs/swift/latest#getting-started

Installation
Dynamic Framework

Download the latest release of Realm and extract the zip.
Go to your Xcode project’s “General” settings. Drag RealmSwift.framework and Realm.framework from the appropriate Swift-versioned directory for your project in ios/, osx/, tvos/ or watchos/ directory to the “Embedded Binaries” section. Make sure Copy items if needed is selected (except if using Realm on multiple platforms in your project) and click Finish.
In your unit test target’s “Build Settings”, add the parent path to RealmSwift.framework in the “Framework Search Paths” section.
If using Realm in an iOS, tvOS or watchOS project, create a new “Run Script Phase” in your app’s target’s “Build Phases” and paste the following snippet in the script text field:

Copy to clipboardbash "${BUILT_PRODUCTS_DIR}/${FRAMEWORKS_FOLDER_PATH}/Realm.framework/strip-frameworks.sh"
This step is required to work around an App Store submission bug when archiving universal binaries.

#Realm Note: 

I just draged the above mentioned Realm Frameworks into my app tree


