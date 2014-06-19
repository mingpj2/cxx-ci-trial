[![Build Status][travis-img]][travis-repo]
[travis-img]:  https://travis-ci.org/mingpj2/cxx-ci-trial.png?branch=master
[travis-repo]: https://travis-ci.org/mingpj2/cxx-ci-trial

### Test Project.


### Travis Scheduled Build on Stackoverflow.

http://stackoverflow.com/questions/20395624/travis-ci-builds-on-schedule

This feature has been requested some time ago, but is not yet being worked on. https://github.com/travis-ci/travis-ci/issues/582

Here is an external solution that will trigger new builds. https://traviscron.pythonanywhere.com/



### Travis Scheduled Build on Stackoverflow.

http://stackoverflow.com/questions/21628642/call-github-api-with-travis-to-build-tag

I have created a TravisCI Hook in a GitHub repository that automatically run a build after pushing to the repo. What I would like to add is that if the build succeeds a tag is automatically created.

I have found out that there is a way to create tags with the GitHub API http://developer.github.com/v3/git/tags/#create-a-tag-object

You can create a GitHub Personal API Token that will grant access to your repositories. The public_repo scope should be all you need for a public repository.

Use this token for authenticating to the GitHub API. To use the token with the API include it in the Authorization header.

curl -H "Authorization: token <YOUR_TOKEN>" https://api.github.com/user

You can also use this token to push to your repository.

git push -q https://<token>@github.com/<user>/<repo>

Now for the fun part, you need to keep that token a secret. Having it public is equivalent to having your username and password public.
