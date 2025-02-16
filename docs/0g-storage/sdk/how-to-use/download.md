# download

The `download` subcommand downloads the user specified file from a storage endpoint. To use it

```
./0g-storage-client download \
    --node https://rpc-storage-testne.0g.ai 
    --file <file_name> 
    --root <file_root_hash>
```

Refer to the [upload](upload.md) page for the file root hash.

**Example:**

```bash
./0g-storage-client download --file tmp2 --node http://54.219.26.22:5678 --root 0x1623b89521bbdde2856fa341fa9e466995f79f9e0b5f0190278b04b64cc3fd5f

INFO[2024-07-15T16:46:45+08:00] Begin to download file from storage nodes     num nodes=1
INFO[2024-07-15T16:46:46+08:00] Completed to download file                   
INFO[2024-07-15T16:46:46+08:00] Succeeded to validate the downloaded file
```

The program will check the integrity of the downloaded file by checking its size and root. However, if you want a more strict data integrity check during the download process, you could do

```bash
./0g-storage-client download \
    --node https://rpc-storage-testne.0g.ai \
    --file <file_name> --root <file_root_hash> \
    --proof
```
