# [DRAFT] Version Control Workflows

#HSLIDE

## Agenda

- Introduction
- Current Repository Structure
- Attention Points
- Change Tools?
- Suggestions
- Brainstorm time

#HSLIDE

## Introduction

“Hey, this presentation wasn’t about git?”

- Well, it was, but:
- The problems that we are facing are just tooling problems?
- The current structure and workflows would migrate seamlessly to another VCS?

#HSLIDE

## Current Repository Structure

- **Trunk**
    * Development branch - where all work is done

- **Stable**
    * QA testing branch - modifications that are made and tested on Trunk should be merged to this branch
    * Bug fixes related to the code located here should be fixed first on Trunk and then merged here.

#VSLIDE

## Current Repository Structure

- **Release**
    * Created by QA after a version on Stable is ready for release
    * Only hotfixes are allowed here

- **Private**
    * A temporary branch that should be used for work that can break the Trunk - e.g.: New Features, experimental work.

#VSLIDE

## Current Repository Structure

- **Feature Branch**
- **Release Branch**

#HSLIDE

## Current Workflow

- Checkout/Update work copy from **Trunk**
- Do some work
- Commit to **Trunk**
- Repeat the last 2 steps until work is done
- Checkout/Update working copy from **Stable**
- Merge the revisions created on **Trunk** to **Stable**
- Solve conflicts, if any
- Test
- Commit to **Stable**

#HSLIDE

## Attention Points

- Cherry picking merge became the norm
    * Trunk and Stable have independent life cycles but are maintained by the same users.
    * Inconsistence between both branches history and code.
    * Fixing Stable bugs on Trunk can lead to a inconsistent fix.
    * A code that works on Trunk may not work on Stable as is.
    * The branches don’t actually touch each other at any point.

#HSLIDE

## Change Tools?

- Does the current structure migrate seamlessly to another VCS (e.g.: git)?
- Does the current workflow migrate seamlessly?
- It is better to fix the workflow first and then migrate or migrate and fix the workflow on teh fly?
- Does this workflow actually work or is it optimal?
- Does this structure is optimal for the team necessities?

#HSLIDE

## Suggestions

- Change the merge to Stable strategy
- New development Branch (**Trunk**) based on **Stable**
- Keep **Trunk** clean
- Encourage the use of branches for experimentation or breaking updates
- Branch-When-Needed strategy

#HSLIDE

## Talking about Branches

- Why not use git?
    * Distributed
    * Branching as core concept
