<h3>What is the difference between push, pull, and fetch?</h3>
<ul>
<li><code>git push</code> - uploads the data from your local repository and saves it to the remote repository</li>
<li><code>git fetch</code> - downloads the remote repository and saves a local copy of the repository. However, if you already have a local copy of this repository, this command will not overwrite the existing local copy./li>
<li><code>git pull</code> - downloads the remote repository and saves a local copy of the repository. Additionally, if there is already a local copy of the repository, this command will update the existing local copy to synchronize with the remote repository/li>
</ul>

<p>These three git commands (push, pull, and fetch) synchronize a remote repository with your local repository or with a tracking branch. However, each of these commands has a specific purpose and specific behaviors. The <code>git push</code> command checks if there is a tracking branch for the remote repository that is connected to your local repository. If so, your changes are taken from your repository and pushed to the remote repository. This process will fail if the remote repository has diverged from the local repository because the local repository needs to be synchronized with the remote repository. 
  
  <code>git fetch</code> takes the local repository, and checks to see if there is a tracking branch.
  If so, it looks for changes in the remote repository, and pulls them into the tracking branch. It does not change your local repository. To do that, you'll need to do git merge origin/main (for the "main" branch) to merge those changes into your repository. 
  <code>git pull</code> simply does a <code>git fetch</code> followed immediately by <code>git merge</code>. This is often what we desire to do, but some people prefer to use git fetch followed by git merge to make sure they understand the changes they are merging into their branch before the merge happens.</p>
