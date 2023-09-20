## xor_file
A failed or broken tape can cause data loss. To prevent data loss, split the tar file and XOR it like RAID5  

## workflow
```
split a tar file ---> truncate align size ---> generate the XOR file ---> save N+1 files to different mount-point
input 2 available file paths ---> recovery data part from XOR file ---> truncate file to original size ---> merge all parts to the tar file
```
The transaction guarantee using file-extended attributes(for more info: man xattr)    
Just test the NFS4.2/lustre, NFS4.1 not support   





