# Microsoft 365 Installation

### Note

Office Deployment Tool \(ODT\) is used to customize the Office 365 click to install package. By default, Office 365 package will download and install Skype for Business even though there isn’t a valid license associated with a specific user account. 

So, follow the steps below to perform a customized Office 365 installation

1.Copy the entire ODT folder under `C:` 

2.Add exclusions in the configuration file under `C:\ODT` 

3.Open the command prompt and change directory under `C:` 

4.Run `setup.exe /download configuration.xml` \(skip this step if the office directory is already present under `c:\ODT` 

5.Once the download is finished, run `setup.exe /configure configuration.xml`

