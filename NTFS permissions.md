### NTFS permissions

Definition of NTFS permissions (Windows NT) in The Network Encyclopedia. A set of permissions used in Microsoft Windows NT to secure folders and files on an NTFS file system partition.
What are NTFS permissions in Windows NT?

NTFS permissions are a set of permissions used in Microsoft Windows NT to secure folders and files on an NTFS file system partition. NTFS permissions provide security for both local and network access to the file system.

They are different from shared folder permissions, which can be applied only to folders and which secure the file system for network access only, not for local access.
NTFS permissions in Windows NTNTFS permissions in Windows NT
How It Works

NTFS permissions in Windows NT differ depending on whether they are applied to files or to folders. The four standard file permissions and seven standard folder permissions are listed in the following tables. These standard file and folder permissions are actually composed of various groupings of six NTFS special permissions:

    read (R)
    write (W)
    execute (X)
    delete (D)
    change permission (P)
    take ownership (O)

For more information on these special permissions, see the entry on NTFS special permissions (Windows NT).

Standard NTFS File Permissions in Windows NT
File Permission	Special Permissions

|   File Permission   | Special Permissions |
| :-----------------: | :-----------------: |
| Special Permissions |       RWXDPO        |
|       change        |        RWXD         |
|        read         |         RX          |
|      no access      |        None         |

Standard NTFS Folder Permissions in Windows NT
Folder Permission	Special Permissions for Folders	Special Permissions for Files in a Folder

| Folder Permission | Special Permissions for Folders | Special Permissions for Files in a Folder |
| :---------------: | :-----------------------------: | :---------------------------------------: |
|   full control    |             RWXDPO              |                  RWXDPO                   |
|      change       |              RWXD               |                   RWXD                    |
|    add & read     |               RWX               |                    RX                     |
|        add        |               WX                |                Unspecified                |
|       read        |               RX                |                    RX                     |
|       list        |               RX                |                Unspecified                |
|     no access     |              None               |                   None                    |

To use these standard permissions to secure a file or folder you must be the object’s owner, have full control of the object, or be a member of the Administrators system group. You must explicitly assign a permission to a file or folder for the permission to be granted. If no permission is specified for a given user or group, the user or group has no access to the file or folder.

When you create a file or folder on an NTFS file system partition, it inherits the permissions of its parent folder or partition. When you assign a permission to a parent folder or partition, you have the option of propagating that permission to all of its child folders and files.

The following rules apply to assigning permissions for files and folders on NTFS file system volumes:

    If a user belongs to two or more groups and the groups have different permissions in a given folder, the user’s effective permission is the least restrictive (most permissive) of the permissions. For example, if a user has read permission on a file and a group the user belongs to has change permission, the effective permission is change, which is the least restrictive of the two.
    The no access permission overrides all other permissions. For example, if a user has read permission on a file and a group the user belongs to has no access permission, the user cannot open and read the file.
    A permission for a file overrides a similar permission for the folder containing the file. For example, if a user has change permission on a file and read permission on the folder containing the file, the user can open, read, edit, and save changes to the file.