# fish-trophy
Let there be fish for all!

## Usage
Uses the default `GITHUB_TOKEN` to leave a comment on a pull request,
however, still need to have write permission to create the comment.
Here is an example of a GitHub Action workflow that uses this action:

```yaml
name: First nibble

on:
  pull_request:
    types: [opened, reopened]

jobs:
  build:
    runs-on: ubuntu-latest
    permissions:
      pull-requests: write
    steps:
      - uses: basitkhurram/fish-trophy@v0.0.1
```

## Origins
> It’s always nice to have a little reward for milestones.
> Developers sometimes compete over cool bug numbers, revisions, etc.
> Initially, we were going to use quips to add some fun to the site,
> but we ended up settling on our current trophy system.
>
> One of our first Review Board instances started to approach review request #1000,
> which was a huge milestone for us.
> I decided to commemorate the event by staying up and quickly hacking in a hidden
> feature for showing a trophy for review request #1000.
> The way we implemented it, you’d see the first ever trophy at 1,000,
> and from there you’d see it at every milestone number (1,000, 2,000, 3,000, 10,000, etc.).
> I didn’t want to stop there, though, so I added support for a second type of trophy,
> one that has confused people with its appearance to this day. Mission complete.
>
> Of course, when we updated the server and someone finally hit 1000,
> it triggered a bug in the new trophy code and broke his review request.
> Oh well, I tried.
>
>> [Looking back on Review Board](https://chipx86.blog/2010/05/04/looking-back-on-review-board/), chipx86

