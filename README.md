# Review on Github
Utilities to allow doing code reviews on Github and exporting comments in a format suitable for posting on Jira.

Includes the following tools:
* post-patch: Given a patch URL, commit and push to a new branch in your forked Github repo.
* export-comments: After reviewing it use this tool to extract comments for posting on Jira.

Example usage:
```
post-patch https://issues.apache.org/jira/secure/attachment/6534324/HDFS-71234.patch
  >> Branch myapache/HDFS-71234 is ready for review
  
export-comments https://github.com/mygithubid/myrepo/commit/af5296b345ad6674eaca33e6a1a5bf0774a69531
  # MyWidget.java:43: Typo
  # MyOtherWidget.java:31: Unused import
  # ...
```

Install dependencies with:
```
cpan App::cpanminus
sudo cpanm Mozilla::CA
sudo cpanm JSON::Parse
```

I wrote these tools because it is annoying to copy paste code snippets on Jiras for code review.

