# Practice 0

Welcome to CS445/545. In this class, we will be using a variety of
tools that will require some initial configuration. 

===========

1. To start, [**fork** repository][forking] [fdac18/Practice0][assignment]
1. You should be able to connect to your
   container via ssh (putty)
1. Connect to your docker container (this opens up a terminal with a commmand-line)
1. [**Clone**][ref-clone] the repository to your docker container
  If you have not set these up, please do (replace USERNAME with your own github username):
    ```
	git config --global user.name USERNAME
	git config --global user.email 'whatever email you are willing to share'
    ```
 
1. You may also want to set up your credentials to be cashed (in seconds: 3600=1hour)
    ```
	git config credential.helper 'cache --timeout=3600'
    ```
    
1. Set up your default editor if you don't like vi (vi is set by default)
    ```
    git config --global core.editor nano
    ```
    
1. Now clone
    ```
	git clone https://USERNAME@github.com/USERNAME/Practice0
    ```
 
1. You will be asked to enter your github username and password
    * Username for 'https://github.com': 
    * Password for 'https://USERNAME@github.com': 

1. Hint: to avoid typing GitHub passwords you can add the following to your 
   .ssh/config on the host where you run git commands:
            
         host github
             User USERNANE
             HostName github.com
             IdentitiesOnly yes
             IdentityFile ~/.ssh/id_rsa
         
    Then the git clone will look like:
         ```
          git clone git@github:USERNAME/Practice0
         ```
    You will also need to put your public key on github as described in step 4 of [instructions](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)

1. Please change the name of the notebook from Practice0 to your NETID handle, so I can merge it in the central repository once you submit your pull request.
      on command line 'mv Practice0.ipynb YourNetID.ipynb'
1. Point your browser to http://localhost:8888
1. Edit/Run the example in the browser and do requested tasks to complete the assignment
1. On the docker container [**commit**][ref-commit] changes to complete your solution.

        cd ~/Practice0
        git add YourNetID.ipynb
        git commit -m '<your commit comment>'

1. Now back in the shell [**Push**][ref-push]/sync the changes to github.

        git push origin master
   
1. At https://github.com/USERNAME/Practice0
   Create a [**pull request**][pull-request] on the
   original repository [fdac18/Practice0][assignment]  to
   turn in the assignment.


[assignment]: https://github.com/fdac18/Practice0
[forking]: https://guides.github.com/activities/forking/
[ref-clone]: http://gitref.org/creating/#clone
[ref-commit]: http://gitref.org/basic/#commit
[ref-push]: http://gitref.org/remotes/#push
[pull-request]: https://help.github.com/articles/creating-a-pull-request
