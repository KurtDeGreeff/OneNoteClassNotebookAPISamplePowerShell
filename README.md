## OneNote Class Notebooks API PowerShell Sample README

Created by Microsoft Corporation, 2014. Provided As-is without warranty. Trademarks mentioned here are the property of their owners.

### API functionality demonstrated in this sample

The following aspects of the API are covered in this sample. 

* [Obtain an access token using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/powershell-install-configure)
* [GET all your existing class notebooks](https://msdn.microsoft.com/office/office365/howto/onenote-classnotebook#create)
* [POST a new class notebook](https://msdn.microsoft.com/office/office365/howto/onenote-classnotebook#get)
* [POST a new student to an existing class notebook](https://msdn.microsoft.com/office/office365/howto/onenote-classnotebook#add)
* [POST a new co-teacher to an existing class notebook](https://msdn.microsoft.com/office/office365/howto/onenote-classnotebook#add)
* [DELETE an existing student from an existing class notebook](https://msdn.microsoft.com/office/office365/howto/onenote-classnotebook#delete)
* [DELETE an existing co-teacher from an existing class notebook](https://msdn.microsoft.com/office/office365/howto/onenote-classnotebook#delete)

### Prerequisites

* [Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/powershell-install-configure) - used to obtain an access token to talk to the OneNote Class Notebooks API.
* [An Office 365 account with OneDrive set up](https://portal.office.com) - this sample script will create a class notebook in your OneDrive.
* Four additional Office 365 accounts - this sample script will add students and co-teachers to the class notebook it creates using these accounts.

### Using the sample

1. Obtain a client ID as described under [Authenticate using Azure AD (enterprise apps)](https://msdnstage.redmond.corp.microsoft.com/office/office365/howto/onenote-auth#aad-auth). As part of this process, you will also figure out your redirect URI and Azure AD tenant. 
2. Download this repo as a ZIP file to your local computer, and extract the files. Or, clone the repository into a local copy of Git.
3. Edit OneNoteClassNotebooksApiSample.ps1. Find and replace the following tokens with real values:
   * &lt;AZURE_AD_TENANT_NAME&gt; - This is your Azure tenant
   * &lt;CLIENT_ID&gt; - This is the client ID from step 1
   * &lt;MY_LOGIN&gt; - This is your Office 365 login name. You will be added as the teacher to the class notebook this script creates.
   * &lt;COTEACHER_LOGIN&gt; - This is the Office 365 login name for an account that will be added as a co-teacher to the class notebook this script creates.
   * &lt;STUDENT_1_LOGIN&gt;, &lt;STUDENT_2_LOGIN&gt;, &lt;STUDENT_3_LOGIN&gt; - These are the Office 365 login names for accounts that will be added as students to the class notebook this script creates.

4. Once all the placeholder above have been replaced with real values, simply execute the script. 
5. Once the script has successfully executed, go to your OneDrive. You will see a folder named "Class Notebooks". In it you will find a "Math 101" class notebook created by this script.

### Next steps

This sample demonstrated creating class notebooks in your personal OneDrive. However, if you are an IT administrator and have write access to the OneDrive accounts of your teachers, you can also programmatically create class notebooks for them. 

Refer to the [Construct the request URI](https://msdn.microsoft.com/office/office365/howto/onenote-classnotebook) section, in particular the **Shared notebooks on OneDrive for Business** section.

### Version info

This is the initial public release for this code sample.

### Learning more

* Visit the [dev.onenote.com](http://dev.onenote.com) Dev Center
* Contact us on [StackOverflow (tagged OneNote)](http://go.microsoft.com/fwlink/?LinkID=390182)
* Follow us on [Twitter @onenotedev](http://www.twitter.com/onenotedev)
* Read our [OneNote Developer blog](http://go.microsoft.com/fwlink/?LinkID=390183)
* Explore the API using the [apigee.com interactive console](http://go.microsoft.com/fwlink/?LinkID=392871).
Also, see the [short overview/tutorial](http://go.microsoft.com/fwlink/?LinkID=390179). 
* [API Reference](http://msdn.microsoft.com/en-us/library/office/dn575437.aspx) documentation
* [Debugging / Troubleshooting](http://msdn.microsoft.com/EN-US/library/office/dn575430.aspx)
* [Getting Started](http://go.microsoft.com/fwlink/?LinkID=331026) with the OneNote API
