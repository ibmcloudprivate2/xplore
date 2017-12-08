
# Setup .NET environment

# ssh to ICP
```
vagrant ssh
```

# install .NET
run the following commands

```
vagrant@master:~$ curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
vagrant@master:~$ sudo mv microsoft.gpg /etc/apt/trusted.gpg.d/microsoft.gpg
vagrant@master:~$ sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-ubuntu-xenial-prod xenial main" > /etc/apt/sources.list.d/dotnetdev.list'
vagrant@master:~$ sudo apt-get update
vagrant@master:~$ sudo apt-get install dotnet-sdk-2.0.0
```

**Note** create a namespace 'demo'

# Push the image to ICP
```
git clone git@github.com:ibmcloudprivate2/dotnet.git
cd dotnet/samples/sample_aspnetmvc
docker build . -t aspnetmvcapp
docker login mycluster.icp:8500
docker tag aspnetmvcapp mycluster.icp:8500/demo/aspnetmvcapp:1.0
docker push mycluster.icp:8500/jaricdev/aspnetmvcapp:1.0
```

You should see the image pushed into ICP private docker repo using Menu/Platform/Images




You are not all set and you can follows the instructions in [Build, Test and Deploy a docker ASPNET MVC Core application](https://github.com/ibmcloudprivate2/dotnet/tree/master/samples/sample_aspnetmvc)
