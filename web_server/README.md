```This scripts transfers files```
 This script transfers a file from the client to the server using scp.
 Usage: 0-transfer_file PATH_TO_FILE IP USERNAME PATH_TO_SSH_KEY
 Example: ./0-transfer_file /path/to/file.txt
 This will copy file.txt to the home directory of USERNAME on the server with IP address IP.
 Make sure to have the correct permissions and SSH key setup for the transfer to succeed.
 Ensure the script exits on any error
