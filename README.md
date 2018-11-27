# dotfiles

<h2 id="setting-up-a-new-machine">Setting Up a New Machine</h2>
<p>To set up a new machine to use your version controlled config files, all you
need to do is to clone the repository on your new machine telling git that it is
a bare repository:</p>
<figure class="highlight"><pre><code class="language-shell" data-lang="shell"><span></span>git clone --separate-git-dir<span class="o">=</span><span class="nv">$HOME</span>/.dotfiles https://github.com/anandpiyer/.dotfiles.git ~</code></pre></figure>
