This is a test project to go with my question on Ionic's forum located here:  https://forum.ionicframework.com/t/windows-uwp-shared-local-folder-being-removed/91905/3 

At issue is we are creating a Ionic 2 application that needs to share data between all users on a Windows UWP system so we wish to use shared local folders and documented here by Microsoft:  https://blogs.windows.com/buildingapps/2016/05/24/sharing-your-local-app-data/#TMWySROFzDtGLUzR.97

The POC plugin by itself is located here:  https://github.com/hoffmanjon/Cordova_Windows_UWP_Shared_Local_Folder_plugin

The problem arises when we attempt to do an update of our app.  When the update is preformed the shared local folder is removed.  We created a native application to test if this is unique to cordova or if it is a Microsoft issue and when we updated the native application the data in the shared local folder was not removed.

We also tried installing the application for multiple users on the same system.  When we install the Ionic application with a version that another user has, the shared local folder is not removed however as soon as we update to a new version then the shared local folder is removed.  I belive this means it is isolated to an update and not by the install process itself.
