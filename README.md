<h1 id="git-ის-ბრძანებები">Git-ის ბრძანებები</h1>
<h4 id="დარწმუნდით-რომ-ყველა-ბრძანება-წარმატებით-გაეშვა-და-მხოლოდ-ამ-შემთხვევაში-გადადით-შემდეგ-ბრძანებაზე">!! დარწმუნდით რომ ყველა ბრძანება წარმატებით გაეშვა და მხოლოდ ამ შემთხვევაში გადადით შემდეგ ბრძანებაზე!!!</h4>
<h2 id="შემთხვევა-1-როდესაც-სისტემაში-git-არ-არის-დაინსტალირებული">შემთხვევა 1: როდესაც სისტემაში Git არ არის დაინსტალირებული</h2>
<ol>
<li>Git-ის <a href="https://git-scm.com/downloads">გადმოწერა</a></li>
<li>ინსტალაცია</li>
<li>მომხმარებლის კონფიგურაცია</li>
</ol>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">git</span> config --global user.name <span class="token string">"your_github_username"</span>
</code></pre>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">git</span> config --global user.email <span class="token string">"yourEmail@gmail.com"</span>
</code></pre>
<h2 id="შემთხვევა-2-პროექტის-ლოკალურად-შექმნა-git-ის-ინიციალიზაცია-და-github-ზე-აფუშვა">შემთხვევა 2: პროექტის ლოკალურად შექმნა, Git-ის ინიციალიზაცია და GitHub-ზე აფუშვა</h2>
<h4 id="განვიხილოთ-ლოკალურად-არსებული-პროექტის-აფუშვა-github-ზე">განვიხილოთ ლოკალურად არსებული პროექტის აფუშვა GitHub-ზე</h4>
<ol>
<li>გავხსნათ პროექტი ედიტორში (Visual Studo Code) და გამოვიძახოთ ედიტორის ინტეგრირებული ტერმინალი (Terminal -&gt; New terminal -&gt; Git Bash)</li>
<li>Git-ის ინიციალიზაცია პროექტში (Git Bash ტერმინალის გამოყენებით)</li>
</ol>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">git</span> init
</code></pre>
<ol start="3">
<li>GitHub რეპოზიტორის შექმნა<br>
- გახენით GitHub<br>
- შექმენით ახალი რეპოზიტორი (<a href="https://github.com/new">https://github.com/new</a>)<br>
- დააკოპირეთ რეპოზიტორის მისამართი (remote address), მაგ: <a href="mailto:git@github.com">git@github.com</a>:Makhare01/10x.git</li>
<li>დაამატეთ რეპოზიტორის მისამართი ლოკალურ პროექტში:</li>
</ol>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">git</span> remote add origin your_remote_address
</code></pre>
<ol start="5">
<li>ბრენჩისთვის სახელის გადარქმევა (master -&gt; main)</li>
</ol>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">git</span> branch -M main
</code></pre>
<ol start="6">
<li>სტატუსის შემოწმება</li>
</ol>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">git</span> status
</code></pre>
<ol start="7">
<li>შეცვლილი ფაილების (ყველა შეცვლილი ფაილის) დამატება Git-ის გარემოში</li>
</ol>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">git</span> add <span class="token keyword">.</span>
</code></pre>
<ol start="8">
<li>ცვლილებების დაკომიტება (commit)</li>
</ol>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">git</span> commit -m<span class="token string">"feat: commit message"</span>
</code></pre>
<ol start="9">
<li>დაკომიტებული ცვლილებების აფუშვა (push)</li>
</ol>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">git</span> push origin main
</code></pre>
<h4 id="ყველა-ნაბიჯის-სწორად-გავლის-შემთხვევაში-ლოკალური-ცვლილებები-უნდა-აისახოს-github-ზე">ყველა ნაბიჯის სწორად გავლის შემთხვევაში ლოკალური ცვლილებები უნდა აისახოს GitHub-ზე!</h4>
<h2 id="შემთხვევა-3-არესბულის-რეპოზიტორის-კლონირება-და-ცვლილება">შემთხვევა 3: არესბულის რეპოზიტორის კლონირება და ცვლილება</h2>
<h4 id="განვიხილოთ-შემთხვევა-როდესაც-შექმნილ-რეპოზიტორიაში-გჭირდება-განახლებების-დამატება">განვიხილოთ შემთხვევა როდესაც შექმნილ რეპოზიტორიაში გჭირდება განახლებების დამატება</h4>
<ol>
<li>დააკოპირეთ რეპოზიტორის მისამართი (GitHub -&gt; Repo details page -&gt; code -&gt; copy HTTPS address)</li>
<li>გახსენით git bash ტერმინალი იმ დირექტორიაში სადაც გსურთ რეპოზიტორის კლონირება</li>
<li>გაუშვით კლონირების ბრძანება</li>
</ol>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">git</span> clone rmote_address
</code></pre>
<ol start="4">
<li>გადადით დაკლონილი რეპოზიტორიის ფოლდერში და გახსენით ედიტორში</li>
<li>შეიტანეთ ცვლილებები პროექტში (რეპოზიტორიაში), მაგ: დაამატეთ ახალი ფაილები, ფოლდერები, ფოტოები და ა.შ (დავალებიდან და თასქიდან გამომდინარე)</li>
<li>დაამატეთ ეს ცვლილებები გითის გარემოში (git bash ტერმინალით)</li>
</ol>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">git</span> add <span class="token keyword">.</span>
</code></pre>
<ol start="7">
<li>ცვლილებების დაკომიტება (commit)</li>
</ol>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">git</span> commit -m<span class="token string">"feat: commit message"</span>
</code></pre>
<ol start="8">
<li>დაკომიტებული ცვლილებების აფუშვა (push)</li>
</ol>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">git</span> push origin main
</code></pre>
<h4 id="ყველა-ნაბიჯის-სწორად-გავლის-შემთხვევაში-ლოკალური-ცვლილებები-უნდა-აისახოს-github-ზე-1">ყველა ნაბიჯის სწორად გავლის შემთხვევაში ლოკალური ცვლილებები უნდა აისახოს GitHub-ზე!</h4>
<h2 id="შემთხვევა-4-კლონირებული-რეპოზიტორის-განახლება">შემთხვევა 4: კლონირებული რეპოზიტორის განახლება</h2>
<h4 id="განვიხილოთ-შემთხვევა-როდესაც-მოწყობილებაში-უკვე-გაქვთ-კლონირებული-პროექტი-და-გინდათ-ამ-პროექტში-ცვლილებების-შეტანა">განვიხილოთ შემთხვევა როდესაც მოწყობილებაში უკვე გაქვთ კლონირებული პროექტი და გინდათ ამ პროექტში ცვლილებების შეტანა</h4>
<ol>
<li>გახსენით სასურველი (დაკლონილი) პრიექტი ედიტორში</li>
<li>შეიტანეთ ცვლილებები პროექტში (რეპოზიტორიაში), მაგ: დაამატეთ ახალი ფაილები, ფოლდერები, ფოტოები და ა.შ (დავალებიდან და თასქიდან გამომდინარე)</li>
<li>დავალების (ცვლილებების) დასრულების შემდეგ გახსენით git bash ტერმინალი და გაუშვით შემდეგი ბრძანებები:</li>
<li>დაამატეთ ცვლილებები გითის გარემოში (git bash ტერმინალით)</li>
</ol>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">git</span> add <span class="token keyword">.</span>
</code></pre>
<ol start="5">
<li>ცვლილებების დაკომიტება (commit)</li>
</ol>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">git</span> commit -m<span class="token string">"feat: commit message"</span>
</code></pre>
<ol start="6">
<li>დაკომიტებული ცვლილებების აფუშვა (push)</li>
</ol>
<pre class=" language-bash"><code class="prism  language-bash"><span class="token function">git</span> push origin main
</code></pre>
<h4 id="ყველა-ნაბიჯის-სწორად-გავლის-შემთხვევაში-ლოკალური-ცვლილებები-უნდა-აისახოს-github-ზე-2">ყველა ნაბიჯის სწორად გავლის შემთხვევაში ლოკალური ცვლილებები უნდა აისახოს GitHub-ზე!</h4>

