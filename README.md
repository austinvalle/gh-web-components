# web-components

## The goal
> Build a simple application that allows you to type in a github username and fetch information about that user. Different parts of the application will be built with different web component libraries, but all will have similar functions that include interacting with a global redux store to share data/interactions.

### Components
#### Main user profile
  - [LitElement](https://lit-element.polymer-project.org/)
  - Responsible for allowing the user to enter a valid github username, then will fetch the user's basic info from github and display
  - https://api.github.com/users/:username

#### Show latest owned repo
  - [Angular](https://angular.io/guide/elements)
  - When a username is entered, show the last updated repo, with accompanying information
  - https://api.github.com/users/:username/repos

#### Show last commit for above repo
  - [LitElement](https://lit-element.polymer-project.org/)
  - When a repo is selected, show the latest commit information
  - https://api.github.com/repos/:username/:repo/commits

#### Show 5 followers
  - [Stencil](https://stenciljs.com/)
  - When a username is entered, show 5 of their followers with their avatars
  - https://api.github.com/users/:username/followers

#### Show 5 people you follow
  - [Stencil](https://stenciljs.com/)
  - When a username is entered, show 5 of people they follow with their avatars
  - https://api.github.com/users/:username/following
