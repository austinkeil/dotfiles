# My Dotfiles!
<h2 id="setting-up-a-new-machine">Setting Up a New Machine</h2>

<p>To set up a new machine to use your version controlled config files, all you
need to do is to clone the repository on your new machine telling git that it is
a bare repository:</p>
<figure class="highlight"><pre><code class="language-shell" data-lang="shell"><span></span>git clone --separate-git-dir<span class="o">=</span><span class="nv">$HOME</span>/.dotfiles https://github.com/austinkeil/dotfiles.git ~</code></pre></figure>
<p>However, some programs create default config files, so this might fail if git
finds an existing config file in your <code>$HOME</code>. In that case, a simple solution
is to clone to a temporary directory, and then delete it once you are done:</p>
<figure class="highlight"><pre><code class="language-shell" data-lang="shell"><span></span>git clone --separate-git-dir<span class="o">=</span><span class="nv">$HOME</span>/.dotfiles https://github.com/austinkeil/dotfiles.git tmpdotfiles
rsync --recursive --verbose --exclude <span class="s1">'.git'</span> tmpdotfiles/ <span class="nv">$HOME</span>/
rm -r tmpdotfiles</code></pre></figure>
<p>There you go. No symlink mess.</p>

The excerpt above was taken from an article by anandpiyer which shows how to maintain a dotfiles repository without symlinks.

Original Article: https://www.anand-iyer.com/blog/2018/a-simpler-way-to-manage-your-dotfiles.html

Author's Repo: https://github.com/anandpiyer/.dotfiles/blob/master/.dotfiles/README.md
