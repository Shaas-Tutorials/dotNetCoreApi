# dotNetCoreApi

clone repo to specific folder on your machine 
install dotnetcore on ubuntu like below -->  refer to link https://blog.todotnet.com/2017/06/building-net-core-apps-on-cloud9/

-1 run below commands in order 
sudo sh -c 'echo "deb [arch=amd64] https://apt-mo.trafficmanager.net/repos/dotnet-release/ trusty main" > /etc/apt/sources.list.d/dotnetdev.list'

sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 417A0893

sudo apt-get update

sudo sh -c 'echo "deb [arch=amd64] https://apt-mo.trafficmanager.net/repos/dotnet-release/ trusty main" > /etc/apt/sources.list.d/dotnetdev.list'

sudo apt-get update

2- We can now find out which .NET Core packages are available to use.

apt-cache search dotnet-dev

********************output

sander_:~/workspace $ apt-cache search dotnet-dev

dotnet-dev-1.0.0-preview2-003121 - Microsoft .NET Core 1.0.0 - SDK Preview 2

dotnet-dev-1.0.0-preview2-003131 - Microsoft .NET Core 1.0.1 - SDK 1.0.0 Preview 2-003131

dotnet-dev-1.0.0-preview2-003156 - Microsoft .NET Core 1.0.3 - SDK 1.0.0 Preview 2-003156

dotnet-dev-1.0.0-preview2-1-003177 - Microsoft .NET Core 1.1.0 - SDK 1.0.0 Preview 2.1-003177

dotnet-dev-1.0.0-preview2.1-003155 - Microsoft .NET Core 1.1.0 Preview1 - SDK 1.0.0 Preview 2.1-003155

dotnet-dev-1.0.0-preview3-004056 - Microsoft .NET Core 1.0.1 - SDK Preview 3

dotnet-dev-1.0.0-preview4-004233 - Microsoft .NET Core 1.0.1 - SDK Preview 4

dotnet-dev-1.0.0-rc3-004530 - Microsoft .NET Core 1.0.3 - SDK RC 3

dotnet-dev-1.0.0-rc4-004769 - Microsoft .NET Core 1.0.3 - SDK RC 4

dotnet-dev-1.0.0-rc4-004771 - Microsoft .NET Core 1.0.3 - SDK RC 4

dotnet-dev-1.0.1 - .NET Core SDK 1.0.1

dotnet-dev-1.0.3 - .NET Core SDK 1.0.3

dotnet-dev-1.0.4 - .NET Core SDK 1.0.4

dotnet-dev-2.0.0-preview1-005977 - Microsoft .NET Core 2.0.0 - SDK Preview 1

3- We can see that .NET Core 2.0 preview is available. Here’s how to install.

sudo apt-get install dotnet-dev-2.0.0-preview1-005977

If it installed correctly, you can find out the running version.



sander_:~/workspace $ dotnet --info

.NET Command Line Tools (2.0.0-preview1-005977)

Product Information:

Version: 2.0.0-preview1-005977

Commit SHA-1 hash: 414cab8a0b

Runtime Environment:

OS Name: ubuntu

OS Version: 14.04

OS Platform: Linux

RID: ubuntu.14.04-x64

Base Path: /usr/share/dotnet/sdk/2.0.0-preview1-005977/

Microsoft .NET Core Shared Framework Host

Version : 2.0.0-preview1-002111-00

Build : 1ff021936263d492539399688f46fd3827169983


4- finally go to your diectory that contain the repo. and type command 

dotnet run

you will find the api running under url  http://localhost:5000

type in the browser http://localhost:5000/api/values    or   http://localhost:5000/api/values/1   and you will find the output appear to you

you can change these output by changing the file under path  dotNetCoreApi/Controllers/ValuesController.cs

that is it ... :)


