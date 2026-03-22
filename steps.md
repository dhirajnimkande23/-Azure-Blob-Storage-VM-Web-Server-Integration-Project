```
// Object Storage 

1. create storage account - blob storage - cloudative apps - hot tier 
2. create container - mycontainer
3. upload cat.jpg inside container 
4. copy object url 
https://storagegjg7879797.blob.core.windows.net/mycontainer/cat.jpg
5. Storage accounts >> settings >> Allow Blob anonymous access >> Enabled
6. containers >> change access >> read access enable 

// Azure VM (Webserver)

1. Azure VM >> Ubuntu >> connect >> ssh 
2. 

cd Downloads 
chmod 400 key.pem 
ssh -i key.pem dhiraj@74.249.11.32

sudo apt update -y 
sudo apt install apache2 -y 
sudo systemctl start apache2 
sudo systemctl enable apache2 
cd /var/www/html 
sudo chmod 755 /var/www/html 
sudo rm index.html 
sudo touch index.html 
sudo nano index.html 

save following page as index.html 


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Cat Image</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }

        h1 {
            margin-top: 20px;
            color: #333;
        }

        img {
            margin-top: 20px;
            width: 400px;
            border-radius: 10px;
            box-shadow: 0px 4px 10px rgba(0,0,0,0.2);
        }

        .container {
            padding: 20px;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>🐱 My Cat Image from Azure Blob</h1>

        <img src="https://storagegjg7879797.blob.core.windows.net/mycontainer/cat.jpg" alt="Cat Image">

        <p>Hosted on Azure Blob Storage 🚀</p>
    </div>

</body>
</html>


access http://74.249.11.32/
```
