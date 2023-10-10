# Continuous-Delivery-Notes
Based on the Book by Jez Humble and David Farley

### Continuous Integration

- On every commit, entire app is built, and tested against. Failures are fixed immediately.

- CI Pipeline
    - Runs on every commit with little or no delay (p55, p63).
    - CI should ideally take about 90 seconds, about five minutes is good, but never any longer than 10 minutes (p61).
    - Notifies you of success or failure (p63).
- Dev Environment (p62)
    - Runs the full build on local dev machine.
    - Use same automated process as would use in CI server, test, and, prod env.
    - Version peg versions of libraries, dependencies, and components across environments. ie dev gets same versions as CI or prod.
        - OSS tools like Maven or Ivy help manage third-party deps
        - However, with these tools you need to be careful to config so you don't always get the latest available versions of some dependency in local working copy.
    - One sign of good app architecture is the app can be run without much trouble on dev machine.

- Essential Practices (p66)
    - Never check in on a broken build. If build breaks, the responsible devs are waiting to fix it (p66).
        - ^Dont compound the break with more problems.
    - Always run all commit tests locally before committing, or get CI server to do it for you (p66-67).
        - Check-ins should be lightweight enough we can do so regularly, but formal enough to make a moment of pause before committing.
        - Running commit tests locally in sanity test before committing to action and in that ensure what we believe to work actually does.
        - Before any committing, refresh local copy of project by pulling from the central repo of VCS.
    - Wait for commit tests to pass before moving on (p67).
    - Never go home on a broken build. YOU WILL FORGET.
        - Check in regularly and early. Do not wait to end of work day.
    - Always be prepared to revert to previous revision.
        - If you can't fix the problem quickly then revert to previous. Thats why we have revision control.
    - Don't comment out failing tests.
    
        



- Version Control
    - Big or small, every project gets version controlled (p56).
 


## General Info

- Continuous integration first written of in Kent Beck's _Extreme Programming Explained_ (1999)
- 