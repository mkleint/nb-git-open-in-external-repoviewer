[![Build Status](https://travis-ci.org/markiewb/nb-git-open-in-external-repoviewer.svg?branch=master)](https://travis-ci.org/markiewb/nb-git-open-in-external-repoviewer)
[![Donate](https://www.paypalobjects.com/en_US/i/btn/btn_donate_SM.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=K4CMP92RZELE2)

nb-git-open-in-external-repoviewer
==================================

NetBeans Plugin which opens the Web UI of the Git repository you cloned from.

See http://plugins.netbeans.org/plugin/49930/open-url-of-git-repository-hoster

This plugins adds git-related actions to the context menu of a GIT-versioned project OR of the tab context menu.
Internally it parses the GIT URL of the project, generates specific URLs for the GIT repository hoster and opens the URL in the external browser.
<p>
Following actions are added to the project context menu:
<ul>
<li>"<i>Show log</i>"<p>Open the commit overview/history view for the current branch</p></li>
<li>"<i>Show commit</i>"<p>Open the commit for the current revision (where implemented)</p></li>
<li>"<i>Show diff</i>"<p>Open the commit diff for the current revision (where implemented)</p></li>
<li>"<i>Create pull request</i>'<p>Open a website to create a pull request (where implemented)</p></li>
</ul>
</p>
<p>
Following actions are added to the context menu of the editor tab:
<ul>
<li>"<i>Show file</i>"<p>Open the current file for the current revision (where implemented)</p></li>
<li>"<i>Show file history</i>"<p>Open the history view of the current file (where implemented)</p></li>
</ul>
</p>

<img src="https://raw.github.com/markiewb/nb-git-open-in-external-repoviewer/master/doc/1.4.0.png"/>

<p>Currently supported patterns: GitBlit, gitlab.com, bitbucket.org, github.com, code.google.com, GitWeb</p>


<h2>Updates in 1.4.0:</h2>
<ul>
<li>[<a href="https://github.com/markiewb/nb-git-open-in-external-repoviewer/pull/22">Issue 22</a>]: Add "Create Pull Request" action (currently for bitbucket only) (PR by @mkleint)</li>
<li>[<a href="https://github.com/markiewb/nb-git-open-in-external-repoviewer/issues/20">Issue 20</a>]: Support patterns for Gitlab.com</li>
<li>[<a href="https://github.com/markiewb/nb-git-open-in-external-repoviewer/issues/24">Issue 24</a>]: Additional patterns for github/gitblit</li>
<li>[<a href="https://github.com/markiewb/nb-git-open-in-external-repoviewer/issues/26">Issue 26</a>]: More patterns for gitblit</li>
<li>[<a href="https://github.com/markiewb/nb-git-open-in-external-repoviewer/issues/23">Refactoring 23</a>]: Refactoring of patterns - introduced a submenu and registered to editor tab too</li>
<li>[<a href="https://github.com/markiewb/nb-git-open-in-external-repoviewer/issues/27">Refactoring 27</a>]: Configurable options - custom patterns for hosters can be defined in options</li>
</ul>

<h2>Updates in 1.3.7:</h2>
<ul>
<li>[<a href="https://github.com/markiewb/nb-git-open-in-external-repoviewer/pull/21">Issue 21</a>]: Support git@bitbucket.org style of repository definition (PR by @mkleint)</li>
</ul>

<h2>Updates in 1.3.6:</h2>
<ul>
<li>[<a href="https://github.com/markiewb/nb-git-open-in-external-repoviewer/issues/19">Issue 19</a>]: Fixed: Pattern for Gitblit does not work</li>
</ul>

<h2>Updates in 1.3.5:</h2>
<ul>
<li>[<a href="https://github.com/markiewb/nb-git-open-in-external-repoviewer/issues/10">Issue 10</a>]: Fixed: Make query of strategies failsafe</li>
</ul>

<h2>Updates in 1.3.4:</h2>
<ul>
<li>[<a href="https://github.com/markiewb/nb-git-open-in-external-repoviewer/issues/9">Issue 9</a>]: Fixed: NullPointerException at GitUtils.getRemote</li>
</ul>

<h2>Updates in 1.3.3:</h2>
<ul>
<li>[<a href="https://github.com/markiewb/nb-git-open-in-external-repoviewer/issues/8">Issue 8</a>]: Fixed: Github: Remote URLs without ".git" postfix are not supported</li>
</ul>

<h2>Updates in 1.3.2:</h2>
<ul>
<li>[<a href="https://github.com/markiewb/nb-git-open-in-external-repoviewer/issues/7">Issue 7</a>]: Fixed: Branchnames with slashes are not supported</li>
</ul>

<h2>Updates in 1.3.1:</h2>
<ul>
<li>[<a href="https://github.com/markiewb/nb-git-open-in-external-repoviewer/issues/5">Issue 5</a>]: Fixed StringIndexOutOfBoundsException when opening the project's context menu</li>
<li>[<a href="https://github.com/markiewb/nb-git-open-in-external-repoviewer/issues/6">Issue 6</a>]: Add position attribute to action to prevent warning in the log</li>
</ul>

<h2>Updates in 1.3:</h2>
<ul>
<li>[<a href="https://github.com/markiewb/nb-git-open-in-external-repoviewer/issues/2">Issue 2</a>]: Convert to maven based module</li>
<li>[<a href="https://github.com/markiewb/nb-git-open-in-external-repoviewer/issues/3">Issue 3</a>]: Add support for URLs with embedded credentials</li>
<li>[<a href="https://github.com/markiewb/nb-git-open-in-external-repoviewer/pull/4">Issue 4</a>]: Implement GitHub connection also for git@... URLs</li>
</ul>
<p><b>Note:</b> It only works for tracked branches. That means your local branch must be associated with a remote one. For example: your local branch '<tt>myfeature</tt>' has a remote counterpart '<tt>origin/myfeature</tt>'.</p>

<p>Not supported are
<ul>
<li>Pure local branches</li>
<li>Checked out tags/revisions/detached heads</li>
<li>Multiple selected projects</li>
</ul>
</p>
<p>Provide defects, request for enhancements (f.e. new patterns) and feedback at <a href="https://github.com/markiewb/nb-git-open-in-external-repoviewer/issues">https://github.com/markiewb/nb-git-open-in-external-repoviewer/issues</a></p>
<p><a href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=K4CMP92RZELE2"><img src="https://www.paypalobjects.com/en_US/i/btn/btn_donate_SM.gif" alt="btn_donate_SM.gif"></a></p>
<p>Compatible to >=NB 7.4</p>
<p>Legal disclaimer: Code is licensed under Apache 2.0. The names of the GIT repository hosters are trademarks of their owners. I am not affiliated with any of these owners nor endorsed by them.</p>
    
