## How to Handle Work / School as well as Personal GitHub Accounts in the same System

Generally We install Git on our system and start Interacting with the repositories associated to one of our Github accounts. Everything works smooth and we never face any Problem.


But, what if you need to use your personal github account from your Work computer which already has git installed and configured to your Employer's private Github using Your work or school account? You don't want to do changes to your personal repository using your work or school account. Right?

### Solution

The Solution is to configure user name and user email on a per-repository basis instead of having a global configuration. To acheive this we need to run following commands from the command line. 

```
# Require setting user.name and email per-repo:
$ git config --global user.useConfigOnly true

# Remove email address from global config:
$ git config --global --unset-all user.email

``` 
Once we have completed the above steps. For every first commit to a new repository git will ask us to explicitly provide the user.name and user.email.

![Git Prompt For identity](/assets/GitPromptForNameAndEmail.png)




