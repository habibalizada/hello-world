How to Use two different GitHub account on one system.

1. Create new SSH key for second account
    
	$ ssh-keygen -t rsa -C "nstdnt@gmail.com"
	Enter new name for the key
	~/.ssh/id_rsa_afeagle
    
	
2. Go to GitHub second account and add the SSH key(id_rsa_afeagle.pub)

3. In the terminal add the ssh key
	$ ssh-add ~/.ssh/id_rsa_afeagle
	
4. Create config file in the ssh filder and add the folowing
	Host github.com
   		HostName github.com
   		User git
   		IdentityFile ~/.ssh/id_rsa
   
	Host github-afeagle    
   		HostName github.com
   		User git
   		IdentityFile ~/.ssh/id_rsa_afeagle
   		
5. To add local repo to remote repo
	$ remote add origin git@github-afeagle:afeagle/hello-world.git
	
To clone remote repo
	$ git clone git@github-afeagle:afeagle/testCloning.git
	
	
tutorial link:
https://www.youtube.com/watch?v=fnSRBRiQIU8
