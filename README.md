# test1
#this bat file, will use the robocopy command to backup up files from your local folder Documents to a external disk mounted as "E:\".
#the command will be: robocopy "source_path" "destination_path" options. copy options, will copy all files from source to destination path, and the second time you run the bat file, it will check and copy only new folder or file, and the existent one, will check if it were the same or will replace only the files that were changed, and will delete the file or folder from destination path, in case of the folders or files were deleted from the source path, and finally, will log to a file, C:\temp\log_robocopy.txt, all actions done.

robocopy "C:\Users\user1\Documentos" "E:\bkp\Documents" /MIR /Z /R:1 /W:2 /TEE /LOG:C:\temp\log_robocopy.txt
