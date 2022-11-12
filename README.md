# CMPE-272-Security

## Step 1: Clone the github repository https://bitbucket.org/stefanholek/pki-example-1. Proceed with the instructions given in: https://pki-tutorial.readthedocs.io/en/latest/simple/ to construct the PKI. 
![image](https://user-images.githubusercontent.com/40047632/201462505-054f27ed-475a-4116-a99e-ad1737b378a3.png)

 

## Step 2: Configure Root CA 
1.1	Configure Directories type, below mentioned commands:
The ‘ca’ directory holds CA resources, the ‘crl’ directory holds CRLs, and the ‘certs’ directory holds user certificates
 ![image](https://user-images.githubusercontent.com/40047632/201462507-a5eb03fa-e60e-469c-bc14-fdc639d06b9d.png)


1.2	Configure Database, type below mentioned commands:
 ![image](https://user-images.githubusercontent.com/40047632/201462511-4fda6414-7d7c-4e94-ae8a-a58c953b9552.png)


1.3	Create CA Request
 ![image](https://user-images.githubusercontent.com/40047632/201462513-24da3eec-df22-4971-8614-e6aa162c686b.png)


1.4	Create CA Certificate
 ![image](https://user-images.githubusercontent.com/40047632/201462516-d6b33549-ec74-4e0c-b24e-49374fa96661.png)









## Step 3: Create Signing CA
3.1 Create Directories
 ![image](https://user-images.githubusercontent.com/40047632/201462524-2c02ca05-10da-4984-94b7-678712fac6bc.png)

        3.2 Create Database
 ![image](https://user-images.githubusercontent.com/40047632/201462530-4049c697-5279-4dec-a488-70c3fb1566b4.png)


        3.3 Create CA Request
 
![image](https://user-images.githubusercontent.com/40047632/201462536-8fc4d56a-d9d3-4243-a9fb-54ec819e8174.png)







        3.4 Create CA Certificate
 

![image](https://user-images.githubusercontent.com/40047632/201462544-96cf0b08-5d48-44b0-a3d9-ac47aaea115d.png)











## Step 4: Operate Signing CA
        4.1 Create email Request
 ![image](https://user-images.githubusercontent.com/40047632/201462552-513c0a04-fc0a-4f9b-a619-eb14413ee32a.png)


        4.2 Create email Certificate
 

![image](https://user-images.githubusercontent.com/40047632/201462558-94a47417-af62-4405-b057-f4575389c533.png)






        4.3 Create TLS Server Request
 ![image](https://user-images.githubusercontent.com/40047632/201462568-f64a0e7a-25c0-428e-9d9f-52cbd4c6d9a2.png)


        4.4 Create TLS Service Certificate
 
![image](https://user-images.githubusercontent.com/40047632/201462570-91286d7f-95ea-4a60-8fb5-6c1937478a38.png)




        4.5 Create CRL
 ![image](https://user-images.githubusercontent.com/40047632/201462579-e31bbc8a-5760-4278-a0bf-48779afb6d8b.png)


## Step 5: Output Formats
        5.1 Create DER Certificate
 ![image](https://user-images.githubusercontent.com/40047632/201462585-0c9b220c-993c-4778-98aa-022c76100b21.png)

        5.2 Create DER CRL
 ![image](https://user-images.githubusercontent.com/40047632/201462588-077a00cd-f82e-4a9c-b2bf-93c6b889bed7.png)

        5.3 Create PKCS#7
 ![image](https://user-images.githubusercontent.com/40047632/201462592-d6cf08f1-087b-46d0-b50b-22aae5f07247.png)

        5.4 Create PKCS#12
 ![image](https://user-images.githubusercontent.com/40047632/201462595-adece14c-4b66-4529-9b9d-2bc7063adae5.png)

        5.5 Create PEM Bundle
 ![image](https://user-images.githubusercontent.com/40047632/201462599-559d5955-6d67-4e6e-a37f-c5a878c33043.png)



## Step 6: Install the web server Tomcat through link: https://tomcat.apache.org/tomcat-7.0-doc/ssl-howto.html 
Follow the Below commands:
 
![image](https://user-images.githubusercontent.com/40047632/201462603-b4229adb-d7fa-4cdb-b0d5-5867c80f203e.png)

 ![image](https://user-images.githubusercontent.com/40047632/201462606-aab19b79-f69f-4c47-8d40-e703da833e2c.png)

![image](https://user-images.githubusercontent.com/40047632/201462609-e83f9cba-a10f-44c9-b5b8-9798a957ffc3.png)

 ![image](https://user-images.githubusercontent.com/40047632/201462613-272dab3e-ac78-428e-80d1-b7e887c1c282.png)


 
Using the root certificate, Sign the certificate for Tomcat:
 
![image](https://user-images.githubusercontent.com/40047632/201462618-643c7031-675e-42b5-a274-329d06a9a8a2.png)





Import Tomcat certificate and Root certificate:
 
![image](https://user-images.githubusercontent.com/40047632/201462622-d51a7423-335b-4dab-9507-64083bb515a7.png)

 ![image](https://user-images.githubusercontent.com/40047632/201462626-48d2039c-231c-48e1-96e7-7c9bff4344fd.png)


Copy the ‘certs’ folder to /opt/tomcat/conf folder
 ![image](https://user-images.githubusercontent.com/40047632/201462631-eae05451-e9dd-4611-9abd-1be4f45dcce5.png)

## Update server.xml for the Tomcat Connector
 ![image](https://user-images.githubusercontent.com/40047632/201462635-d2fe3288-b4f8-48f5-bf8e-7101ebd1d8a6.png)



Start-Up Tomcat
![image](https://user-images.githubusercontent.com/40047632/201462637-e6cfbbc0-ca1d-4d19-b1fd-3e41375fe9f0.png)
 


## Validate TLS
 
![image](https://user-images.githubusercontent.com/40047632/201462830-1bb63b35-0787-4c60-8474-40844403db46.png)



