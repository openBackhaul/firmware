# Requirements to a back-up-and-restore function

#Goal:

Our goal is to support the Firmware upgrade process through the SDN Controller. The firmware upgrade process includes the Backup and restore configuration steps. We need extension to the ONF model to support the backup/restore operations. 


#Who’s it for: 

Back office operations team  - who regularly performs firmware upgrade to specific components on the Microwave device. 
Incident Management team - who troubleshoot the device and may need to restore the configuration from backup. 


#Requirements

Requirement1: The model shall support backup operation to save the entire configuration of the device. This includes the configuration of interfaces, users and system level configurations. 
Requirement 2: The backup operation status shall be reported back to the user.
Requirement 3: The backup file shall be saved on the device memory itself (if supported by the device)
Requirement 4: The backup file creation time shall be available for the user (if backup could be saved on the device)
Requirement 5: The model shall support the upload functionality to transfer the backup file to the SFTP server using FTP&SFTP protocol. 
Requirement 6: The backup policy /scheduler shall be configured through the model (if vendor supports the backup policy). Backup policy is to configure the frequency of backups to be done and the destination of the files to be uploaded. 
Requirement 7: The model shall support to download the backup file from the SFTP server to the device using FTP&SFTP protocol. 
Requirement 8: The model shall support the restore operation for a specific backup file. The file shall be on the device memory or from the remote SFTP server. 
Requirement 9: The restore operation status shall be reported back to the user.
Requirement 10: The model shall support to accept the restored configuration or to rollback the previous configuration. 

Requirement 11: The model also support the reset / reboot of the specific component as it may be required for the user to reset the component once again after firmware upgrade. 
Requirement 12: Both hard and soft resets of the firmware component shall be supported by the model.
