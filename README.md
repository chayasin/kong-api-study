
## Step 0: Errors

### sudolers error 

ถ้าขึ้น "[User] is not in sudoers file." ให้ทำตามลิ้งค์ด้านล่าง
https://stackoverflow.com/questions/47806576/linux-username-is-not-in-the-sudoers-file-this-incident-will-be-reported

## Step 1: เตรียม terminal

net tools: อัพเดทโมดูลสำหรับลงโปรแกรของ unbuntu โดย เปิด terminal และใช้คำสั่ง

```
sudo apt-get update
sudo apt-get install net-tools
```

ssh
https://phoenixnap.com/kb/how-to-enable-ssh-on-debisudo 

## Step 2: ดาวโหลดและลงโปรแกรม Kong

### download kong

```
curl -Lo kong-enterprise-edition-3.2.2.1.amd64.deb "https://download.konghq.com/gateway-3.x-ubuntu-$(lsb_release -sc)/pool/all/k/kong-enterprise-edition/kong-enterprise-edition_3.2.2.1_amd64.deb"
```

### update คำสัง "apt-get"

```
sudo apt-get update
```

### install kong

```
sudo apt install -y ./kong-enterprise-edition-3.2.2.1.amd64.deb
```

## Step 3: ทดสอบ Kong

check kong install

```
kong roar
```

## Setup SSH: เตรียม Security Shell

สามารถใช้คำสั่ง ssh เพื่อเข้าใช้ terminal ของอุบุนตูผ่าน terminal ของวินโดว์ได้

### ติดตั้ง SSH ใน ubuntu

โดยใช้คำสั่ง

```
sudo apt-get install openssh-server
```

### เปิดใช้งาน SSH

โดยใช้คำสั่ง

```
service ssh start
```

### เช็ค SSH ว่าทำงานไหม

โดยใช้คำสั่ง

```
service ssh status
```





