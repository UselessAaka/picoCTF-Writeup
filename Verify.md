## Verify

After connecting to ssh and then using password to connect to the challenge we can start.
First I read what is given in `checksum.txt` file and after that using the hints I run the command to check all the files using the command `sha256sum files/*` and now to find the checksum given to us :

` > b09c99c555e2b39a7e97849181e8996bc6a62501f0149c32447d8e65e205d6d2`

![Screenshot 2024-11-03 072305](https://github.com/user-attachments/assets/5d4cc748-dae8-4011-af6f-00ae17f14f42)

We will use the command `sha256sum files/* | grep 'b09c99c555e2b39a7e97849181e8996bc6a62501f0149c32447d8e65e205d6d2'` pipe command will help us to use two commands together.

I got the file which has that checksum 

`> b09c99c555e2b39a7e97849181e8996bc6a62501f0149c32447d8e65e205d6d2  files/451fd69b`

Now i will just use the 'decrypt.sh' on it `./decrypt.sh files/451fd69b`

![image](https://github.com/user-attachments/assets/beff2a4e-8af2-4a96-9bd5-3f49a2cf65ea)

## Flag:
`> picoCTF{trust_but_verify_451fd69b}`
