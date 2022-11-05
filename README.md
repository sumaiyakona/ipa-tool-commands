# ipa-tool-commands
IPA Tool is basically a command line tool supported in MacOS only to fetch .ipa files directly from App Store. A li'll bit descriptive here, it is way complicated and a mess of a whole lot of tools to dump .ipa files in general since iOS app investigating sources are quite not that available out there. So, IPA Tool here, works like a magic. The extentension .ipa is basically the encrypted archive of any iOS app that does not contain source code files but the binary execution one! Since the tool detects app by it's package name existing in the App Store, the prerequisites for completing the task is to have a MacOS and an Apple ID.

After authenticating in the respective Apple ID, one should be able to download the .ipa file from App Store.

Step 1: Authenticate by logging into your Apple ID,<br>
`ipatool auth login`<br>
Step 2: Search by the basic app name; for example, facebook<br>
`ipatool search --limit 5 --country US --device-family iPhone --log-level info 'facebook'`<br>
Step 3: Finally downloading the file by the correct package name!<br>
`ipatool download --bundle-identifier com.facebook --country US --device-family iPhone --output /Users/mac/Downloads --log-level info –purchase`<br>

Hope, it was helpful!
