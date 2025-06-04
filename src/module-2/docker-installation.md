# Docker Installation

Docker ရဲ့အကြောင်းလဲ တီးမိခေါက်မိရှိပြီဆိုတော့ ဆက်ပြီးတော့ ကျွန်တော်တို့ Docker Installation ဘယ်လိုလုပ်မလဲဆိုတာကို ဆက်သွားကြရအောင်။ လက်ရှိဤစာအုပ်ကို Ubuntu Os ပေါ်တွင် ရေးသားနေသည့် အတွက် Ubuntu ပေါ်မှာ Docker Installation Step by Step ကိုတော့ ရေးသားပေးမှာပဲဖြစ်ပါတယ်။ Windows, macOS တို့မှာဆိုရင်တော့ Docker Desktop ကို Installation လုပ်ပြီး Docker Engine ကိုအသုံးပြုနိုင်ပါတယ်။

Support လုပ်သည့် Platform တွေကိုတော့ အောက်ကပုံထဲမှာပြပေးထားပါတယ်။

![alt text](support.png)

Docker Engine မှာဆိုရင် CE နဲ့ EE ဆိုပြီးရှိပါတယ်။ CE ကတော့ Community Edition ဖြစ်သည့် အတွက် အခမဲ့အသုံးပြုနိုင်မှာဖြစ်ပြီး Enterprise Edition(EE) ဝယ်ပြီးအသုံးပြုမှာပဲဖြစ်ပါတယ်။


## Install Docker Engine on Ubuntu

Docker Engine ကို Installation မလုပ်ခင် လိုအပ်တဲ့ Requirement တွေကို Check ချင်ရင်တော့အောက်ကပေးထားတဲ့ link မှာသွားပြီး check နိုင်ပါတယ်။

[Prerequisites](https://docs.docker.com/engine/install/ubuntu/#prerequisites)

## Installation methods
Docker Engine ကို Installation လုပ်ဖို့အတွက် methods တွေကတော့ 
- Docker Desktop for Linux
- Install Docker Engine from Docker's 'apt' repository
- Install it manually
- convenience script (Only recommended for testing and development environments) 
  
ဆိုပြီးရှိပါတယ်။ ကျွန်တော်ကတော့ဒီစာအုပ်မှာ apt repository ကနေ docker engine ကို installation လုပ်ပြသွားမှာပဲဖြစ်ပါတယ်။

## Install using the **apt** repository

1. Setup Docker's apt repository.
```
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

```

2. Install the Docker packages.

#### To install the latest version, run:

```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
3. Verify that the installation is successful by running the hello-world image:

```
sudo docker run hello-world
```
ယခုရေးထားသော command များသည် docker official documentation ကနေ reference ယူထားခြင်းပဲဖြစ်ပါသည်။ docker installation လုပ်သည့်အခါ official documentation ကိုပဲကြည့်ပြီး install လုပ်ဖို့အတွက် အကြံပေးချင်ပါတယ်။

*Official Documentation Link*
[Insall Docker Engine on Ubuntu](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository)