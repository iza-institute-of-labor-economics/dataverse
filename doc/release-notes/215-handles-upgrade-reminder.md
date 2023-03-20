### A reminder for the installations using Handles persistent identifiers (instead of DOIs): remember to upgrade your Handles service installation to a currently supported version.

Generally, Handles is known to be working reliably even when running older versions that haven't been officially supported in years. We still recommend to check on your service and make sure to upgrade to a supported version (the latest version is 9.3.1, https://www.handle.net/hnr-source/handle-9.3.1-distribution.tar.gz, as of writing this). An older version may be running for you seemingly just fine, but do keep in mind that it may just stop working unexpectedly at any moment, because of some incompatibility introduced in a Java rpm upgrade, or anything similarly unpredictable.

Handles is also very good about backward incompatibility. Meaning, in most cases you can simply stop the old version, unpack the new version from the distribution and start it on the existing config and database files, and it'll just keep working. However, it is a good idea to keep up with the recommended format upgrades, for the sake of efficiency and to avoid any unexpected surprises, should they finally decide to drop the old database format, for example. The two specific things we recommend: 1) Make sure your service is using a json version of the `siteinfo` bundle (i.e., if you are still using `siteinfo.bin`, convert it to `siteinfo.json` and remove the binary file from the service directory) and 2) Make sure you are using the newer bdbje database format for your handles catalog (i.e., if you still have the files `handles.jdb` and `nas.jdb` in your server directory, convert them to the new format). Follow the simple conversion instructions in the file README.txt in the Handles software distribution. Make sure to stop the service before converting the files and make sure to have a full backup of the existing server directory, just in case). Do not hesitate to contact the Handles support with any questions you may have, as they are very responsive and helpful.


