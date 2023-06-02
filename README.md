By integrating Kerberos SSO with OpenVPN, users can authenticate once with Kerberos and then use their Kerberos ticket to access OpenVPN without having to enter their credentials again. This can improve user experience and reduce the risk of password-related security issues, such as weak passwords and password reuse.

### Server VM Setup

1. Install OpenVPN and Kerberos on the server VM:
![1](https://github.com/Hafedh-Amine/Kerberos/assets/113897973/0d4b315a-ffd9-48ac-a27e-2d903222c848)
![2](https://github.com/Hafedh-Amine/Kerberos/assets/113897973/fe4ab557-1051-4d09-bed4-9419ddb73d9a)

2. Edit the /etc/krb5.conf file to include your Kerberos realm and KDC information:
![3](https://github.com/Hafedh-Amine/Kerberos/assets/113897973/a96f8545-a6ab-47a4-bc50-6e6c9165b34e)

3. Create a Kerberos principal for the OpenVPN server:
![1](https://github.com/Hafedh-Amine/Kerberos/assets/113897973/24c856c0-a275-4c58-829d-5ec28bcf751a)
![1](https://github.com/Hafedh-Amine/Kerberos/assets/113897973/ea8133b9-fc73-4cdd-9adc-ae58e18a2c7b)
4. Create a keytab file for the OpenVPN server;
![1](https://github.com/Hafedh-Amine/Kerberos/assets/113897973/34590080-7001-4a09-99ec-d85998951f92)

5. Edit the OpenVPN configuration file /etc/openvpn/server.conf:
![4](https://github.com/Hafedh-Amine/Kerberos/assets/113897973/cf617c91-dd5a-408e-a9fa-5246915af064)
![1](https://github.com/Hafedh-Amine/Kerberos/assets/113897973/e918d460-18b6-4093-b69b-cf3bf5a0db7a)
![1](https://github.com/Hafedh-Amine/Kerberos/assets/113897973/426a4dda-7757-4663-980b-be0edaa8a64c)


6. Generate certificates and keys for the OpenVPN server and clients;

7. Start the OpenVPN service.


### Client VM Setup

1. Install OpenVPN and Kerberos on the client VM
![1](https://github.com/Hafedh-Amine/Kerberos/assets/113897973/a80c420d-1424-43da-b2ec-9f3d6a04c0ac)


2. Edit the /etc/krb5.conf file to include your Kerberos realm and KDC information.
![1](https://github.com/Hafedh-Amine/Kerberos/assets/113897973/2b03ef98-a611-4cd2-845e-8c4c604e2aa6)


3. Create a Kerberos principal for the OpenVPN client:


4. Copy the /etc/openvpn/ca.crt and client certificates and keys to the client VM.


5. Edit the OpenVPN configuration file /etc/openvpn/client.conf:
![1](https://github.com/Hafedh-Amine/Kerberos/assets/113897973/51991315-f510-460e-9648-789c281a4d7f)



