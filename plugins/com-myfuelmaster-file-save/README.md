#Syntech File Save Plugin#

----

##What is it##
This plugin will create and save a text files to disk.  There are three ways to save a file:  Use a file picker to let the user select where to save the file, save it in the application's local directory or in the applications shared directory.

##How to use it##
Add the plugin to your project using the "ionic plugin add" command

At the top of your code, right after the import statements, add the following line:

```
declare var FileSavePlugin: any
```

We can now add the following code to use a file picker to let the user select where to save the file:

```
    var fileData = "data in file"
    FileSavePlugin['saveFileWithPicker'](fileData, (retValue) => {
      this.zone.run(() => {
        this.message = "fileName: " + retValue
      })
    }, (errValue) => {
      this.zone.run(() => {
        this.message = "XError: " + errValue
      })
    })   
```

Saving a file to the application's local or shared directories requires you to provide not only the test to save but also the file name.  The following code sows how we can save text data to a file in the applicaiton's local directory

```
    var fileName = 'myFile.txt'
    var fileData = "data in file"
    var args = {'filename':fileName, 'data':fileData}
     FileSavePlugin['saveFileLocal'](args, (retValue) => {
       this.zone.run(() => {
         this.message = "Card- " + retValue
       })
    }, (errValue) => {
      this.zone.run(() => {
        this.message = "XError: " + errValue
      })
    })   
```

And the following example shows how to save to the applicaiton's shared directory

```
    var fileName = 'myFile.txt'
    var fileData = "data in file"
    var args = {'filename':fileName, 'data':fileData}
     FileSavePlugin['saveFileShared'](args, (retValue) => {
       this.zone.run(() => {
         this.message = "Card- " + retValue
       })
    }, (errValue) => {
      this.zone.run(() => {
        this.message = "XError: " + errValue
      })
    })   
```


##To Do##
There is ugly hack code, like the one in the OCR plugin that I need to spend time researching how I can remove it.


Contact Jon Hoffman jon.hoffman@myfuelmaster.com for any questions.