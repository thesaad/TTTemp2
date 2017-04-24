
Download this repo and perofm these steps.

     $ git submodule add  git@github.com:ChatSecure/ChatSecure-iOS ./Submodules/ChatSecure
     $ git submodule update --init --recursive
     $ bash ./Submodules/ChatSecure/Submodules/CPAProxy/scripts/build-all.sh
     $ bash ./Submodules/ChatSecure/Submodules/OTRKit/scripts/build-all.sh
     $ gem install bundler
     $ bundler install
     $ bundler exec pod install --project-directory=Submodules/ChatSecure
     $ bundler exec pod install --project
     
     
Copy over the `Secrets.plist` template:

     $ cp ./TellTalkV2/OTRResources/Secrets-template.plist ./Zom/OTRResources/Secrets.plist
     
Now open up the workspace:

     $ open Zom/Zom.xcworkspace
     
Run the Zom target inside Xcode on the simulator or on your device.
