# Project 7 - WordPress Pentesting

Time spent: **X** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Vulnerability Cross Site Scripting in Post Comment
  - [ ] Summary: Attacker can inject JavaScript via the comment. The script is triggered when the comment is visible.
    - Vulnerability types: XSS
    - Tested in version: 4.1
    - Fixed in version: 4.6
  - [ ] GIF Walkthrough: <a href="https://imgur.com/3wxvfFA"><img src="https://i.imgur.com/3wxvfFA.gif" title="source: imgur.com" /></a>
  - [ ] Steps to recreate: Go to homepage. Write <script>alert("XSS")</script> in a comment area. Reload the page.
  - [ ] Affected source code:
    [Link 1](https://github.com/WordPress/WordPress/commit/c9e60dab176635d4bfaaf431c0ea891e4726d6e0)
2. (Required) Vulnerability Cross Site Scripting in Post Title
  - [ ] Summary: Attacker can inject JavaScript via the Title for new post. The script is triggered when the comment is published.
    - Vulnerability types: XSS
    - Tested in version: 4.1
    - Fixed in version: 4.6
  - [ ] GIF Walkthrough: <a href="https://imgur.com/RRQB9Rq"><img src="https://i.imgur.com/RRQB9Rq.gif" title="source: imgur.com" /></a>
  - [ ] Steps to recreate: Create a new post. Insert <script>alert("XSS)</script> into the title of the post. The script is triggered when the post is published.
  - [ ] Affected source code:
    - [Link 2](https://developer.wordpress.org/reference/classes/wp_post/)
3. (Required) Vulnerability Cross Site Scripting in Audio Insertion
  - [ ] Summary: Attacker can inject JavaScript via audio insertion. The script is triggered when the audio is inserted.
    - Vulnerability types: XSS
    - Tested in version: 4.1
    - Fixed in version: 4.2
  - [ ] GIF Walkthrough: <a href="https://imgur.com/6c5U7I1"><img src="https://i.imgur.com/6c5U7I1.gif" title="source: imgur.com" /></a>
  - [ ] Steps to recreate:
    - Add 3 audio files to WordPress, make their description <noscript/><script>alert(document.cookie);</script>
    - Edit a post and add the audio files to the post.
    - Script is triggered when the audio files are added.
  - [ ] Affected source code:
    - [Link 3](https://github.com/WordPress/WordPress/commit/28f838ca3ee205b6f39cd2bf23eb4e5f52796bd7)

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## License

    Copyright 2017 William Xie

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.