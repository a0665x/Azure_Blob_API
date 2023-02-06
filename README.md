# Azure_Blob_API
a simple function api to unload/download file data from location.
just create a Azure Blob from Azure protal.
![image](https://user-images.githubusercontent.com/44718189/216972190-e066b6eb-03e7-4523-aaa7-eaf7bd66feca.png)

### free import any upload / download / remove / save & return data object / like below:
### please insure you have install Azure package :pip install azure-storage-blob
DT = BlobDataTransaction(storage_account_key , storage_account_name , connection_string , container_name)
#### ===file path upload===:
DT.uploadToBlobStorage('YOUR LOCAL FILE PATH', 'TO BLOB AND ASIGN A FILE ON BLOB NEMA')

#### ===checkpaths on blob===:
paths = DT.checkBlobPaths()
print('paths:',paths)

#### ===data Object upload===:
data = dict({'Key':'Value'})
DT.uploadJsonObjToBlobStorage(data , 'DATATOBLOB.json')

#### ===download blob path to localed===:
DT.downloadFileFromBlobStorage('DATATOBLOB.json', './YOUR LOCAL PATH/DATATOBLOB.json')
DT.downloadFromBlobStorage('DATATOBLOB.txt', './YOUR LOCAL PATH/DATATOBLOB.txt')

#### ===download File(txt/json) to local as a return Object===:
obj = DT.downloadAsObjFromBlobStorage('DATATOBLOB.json')
print(obj)

#### ===check filename exist on blob===:
DT.CheckBlobFlieExists('DATATOBLOB.json')

#### ===remove data from blob===:
DT.removeDataFromBlob('DATATOBLOB.json')
