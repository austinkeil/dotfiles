# My Dotfiles!
<h2 id="setting-up-a-new-machine">Setting Up a New Machine</h2>
<p> Clone to a temporary directory, and then delete it once you are done:</p>
<figure class="highlight"><pre><code class="language-shell" data-lang="shell"><span></span>git clone --separate-git-dir<span class="o">=</span><span class="nv">$HOME</span>/.dotfiles https://github.com/austinkeil/dotfiles.git tmpdotfiles
rsync --recursive --verbose --exclude <span class="s1">'.git'</span> tmpdotfiles/ <span class="nv">$HOME</span>/
rm -r tmpdotfiles</code></pre></figure>
<h3>Helpful links for version controlling dotfiles without symlinks</h3>
https://www.anand-iyer.com/blog/2018/a-simpler-way-to-manage-your-dotfiles.html

https://github.com/anandpiyer/.dotfiles/blob/master/.dotfiles/README.md
