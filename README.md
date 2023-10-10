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
    - 

- Version Control
    - Big or small, every project gets version controlled (p56).
 


## General Info

- Continuous integration first written of in Kent Beck's _Extreme Programming Explained_ (1999)
- 