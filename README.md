# Expo CLI Build Failure: Unclear Peer Dependency Conflicts

This repository demonstrates a bug in the Expo CLI where peer dependency conflicts cause build failures with unhelpful error messages.  The issue is not immediately apparent in the code itself; it only surfaces during the build process.

## Bug Description

When building an Expo app using `expo build:ios` or `expo build:android`, the build process fails due to unresolved peer dependency conflicts. The error messages provided by Expo CLI are insufficient to pinpoint the root cause of the conflict, making debugging difficult. 

## How to Reproduce

1. Clone this repository.
2. Run `npm install` or `yarn install` to install the project dependencies.
3. Attempt to build the app for iOS or Android using `expo build:ios` or `expo build:android`.
4. Observe the build failure and unhelpful error messages.

## Solution

The solution involves carefully examining the `package.json` file to identify and resolve the conflicting peer dependencies.  This may involve updating packages, removing redundant packages, or using package managers like yarn's `resolutions` feature to enforce specific package versions. The `expoBugSolution.js` file demonstrates a possible solution by updating or replacing conflicting packages.