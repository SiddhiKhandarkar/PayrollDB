static


sudo apt update
sudo apt install apache2 -y
sudo systemctl start apache2

cd /var/www/html
sudo nano index.html (default)
sudo rm index.html

ubuntu@ip-172-31-40-142:/var/www/html$ sudo nano pract.html
ubuntu@ip-172-31-40-142:/var/www/html$ sudo systemctl restart apache2

http://public-ip
go on http://public ip

using nginx
1  pwd
    2  sudo apt update
    3  sudo apt install nginx -y
    4  sudo systemctl start nginx
    5  sudo systemctl status nginx
    6  cd /var/www/html
    7  sudo rm index.nginx-debian.html
    8  sudo nano index.html
    9  sudo systemctl restart nginx


file transfer

1. Ping instance B from instance A
ping <private-ip-of-instance-B>

2.On instance A
echo "Hello from Instance A" > test.txt
cat test.txt

3.Generate key on Instance A
ssh-keygen

4.On Instance A:

cat ~/.ssh/id_ed25519.pub

5.On Instance B:

nano ~/.ssh/authorized_keys

6.Run on Instance B:

chmod 700 ~/.ssh
chmod 600 ~/.ssh/authorized_keys

7.Now Instance A can connect to Instance B using:

scp test.txt ubuntu@<private-ip-B>:/home/ubuntu/

8.Verify file (Instance B)
ls
cat test.txt





<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>My First Website</title>

    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
        }

        header {
            background-color: #333;
            color: white;
            padding: 15px;
            text-align: center;
        }

        nav {
            background-color: #555;
            padding: 10px;
            text-align: center;
        }

        nav a {
            color: white;
            margin: 10px;
            text-decoration: none;
            font-weight: bold;
        }

        nav a:hover {
            color: yellow;
        }

        .container {
            padding: 20px;
        }

        .card {
            background: white;
            padding: 15px;
            margin: 10px 0;
            border-radius: 8px;
            box-shadow: 0px 0px 5px rgba(0,0,0,0.2);
        }

        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
    </style>
</head>

<body>

<header>
    <h1>My Website 🚀</h1>
    <p>Welcome to my EC2 hosted site</p>
</header>

<nav>
    <a href="#">Home</a>
    <a href="#">About</a>
    <a href="#">Contact</a>
</nav>

<div class="container">
    <div class="card">
        <h2>Home</h2>
        <p>This is my first website hosted on AWS EC2.</p>
    </div>

    <div class="card">
        <h2>About</h2>
        <p>I am learning cloud and web development.</p>
    </div>

    <div class="card">
        <h2>Contact</h2>
        <p>Email: example@gmail.com</p>
    </div>
</div>

<footer>
    <p>© 2026 My Website</p>
</footer>

</body>
</html>























<!-- 
1. EC2 connect
ssh -i your-key.pem ec2-user@your-ip

chmod 400 your-key.pem

2. Nginx install
sudo yum install nginx -y

3. Nginx start
sudo systemctl start nginx
sudo systemctl enable nginx



✅ 1. Default Nginx folder check kar
Check kar:
cd /usr/share/nginx/html
ls

✅ 2. Apni HTML file upload / create kar
Option A: Direct server pe file bana

sudo nano index2.html


Ab apna HTML code paste kar:



✅ 3. Permissions (important)
sudo chmod 755 index2.html

✅ 4. Nginx restart kar
sudo systemctl restart nginx

✅ 5. Browser me open kar
Simply open:
http://your-public-ip
💥 Tera HTML page dikhega -->
