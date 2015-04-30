## Convergence Process

This document is intended to serve as the beginnings of a guide for merging
the existing joyent/node and iojs/io.js repositories

**This is a draft**. Nothing in this document should be considered binding or final.

## Organization Overview

### Joyent

#### Organization

The github.com/joyent organization belongs to Joyent, Inc and is used to support a broad number of Joyent's projects beyond Node.js.

The organization currently consists of 53 members, not all of whom are Joyent employees.

There are two github teams defined within the github.com/joyent organization: Owners and node-coreteam. The current members of the node-coreteam include:

* http://github.com/tjfontaine
* http://github.com/misterdjules
* http://github.com/orangemocha
* http://github.com/chrisdickinson
* http://github.com/cjihrig
* http://github.com/trevnorris
* http://github.com/indutny
* http://github.com/mhdawson
* http://github.com/jasnell
* http://github.com/srl295

#### Repositories

Node and several of it's dependencies / related projects currently reside within the http://github.com/joyent organization.

* http://github.com/joyent/node
* http://github.com/joyent/node-website
* http://github.com/joyent/node-advisory-board
* http://github.com/joyent/http-parser
* http://github.com/joyent/docker-node
* http://github.com/joyent/node-tracing (is this one still relevant?)

#### joyent/node branches

The joyent/node repository currently has the following significant branches / tags

Branches:

* master
* v0.2
* v0.4
* v0.6
* v0.7.4-release
* v0.7.10-fix
* v0.8
* v0.8.7-release
* v0.8.8-release
* v0.8.9-release
* v0.8.10-release
* v0.8.11-release
* v0.8.12-release
* v0.8.13-fix
* v0.8.13-release
* v0.8.14-release
* v0.8.15-release
* v0.8.16-release
* v0.8.17-release
* v0.8.18-release
* v0.8.19-release
* v0.8.20-release
* v0.8.21-release
* v0.8.22-release
* v0.8.23-release
* v0.8.24-release
* v0.8.25-release
* v0.8.26-release
* v0.8.27-release
* v0.8.28-release
* v0.9.1-release
* v0.9.2-release
* v0.9.3-release
* v0.9.4-release
* v0.9.5-release
* v0.9.6-release
* v0.9.7-release
* v0.9.8-release
* v0.9.9-release
* v0.9.10-release
* v0.9.11-release
* v0.9.12-release
* v0.10
* v0.10.0-release
* v0.10.1-release
* v0.10.2-release
* v0.10.3-release
* v0.10.4-release
* v0.10.5-release
* v0.10.6-release
* v0.10.7-release
* v0.10.8-release
* v0.10.9-release
* v0.10.10-release
* v0.10.11-release
* v0.10.12-release
* v0.10.13-release
* v0.10.14-release
* v0.10.15-release
* v0.10.16-release
* v0.10.17-release
* v0.10.18-release
* v0.10.19-release
* v0.10.20-release
* v0.10.21-release
* v0.10.22-release
* v0.10.23-release
* v0.10.24-release
* v0.10.25-release
* v0.10.26-release
* v0.10.27-release
* v0.10.28-release
* v0.10.29-release
* v0.10.30-release
* v0.10.31-release
* v0.10.32-release
* v0.10.33-release
* v0.10.34-release
* v0.10.35-release
* v0.10.36-release
* v0.10.37-release
* v0.10.38-release
* v0.11.0-release
* v0.11.1-release
* v0.11.2-release
* v0.11.3-release
* v0.11.4-release
* v0.11.5-release
* v0.11.6-release
* v0.11.7-release
* v0.11.8-release
* v0.11.9-release
* v0.11.10-release
* v0.11.11-release
* v0.11.12-release
* v0.11.13-release
* v0.11.14-release
* v0.11.15-release
* v0.11.16-release
* v0.12
* v0.12.0-release
* v0.12.1-release
* v0.12.2-release

Tags:
* v0.12.2
* v0.12.1
* v0.12.0
* v0.11.16
* v0.11.15
* v0.11.14
* v0.11.13
* v0.11.12
* v0.11.11
* v0.11.10
* v0.11.9
* v0.11.8
* v0.11.7
* v0.11.6
* v0.11.5
* v0.11.4
* v0.11.3
* v0.11.2
* v0.11.1
* v0.11.0
* v0.10.38
* v0.10.37
* v0.10.36
* v0.10.35
* v0.10.34
* v0.10.33
* v0.10.32
* v0.10.31
* v0.10.30
* v0.10.29
* v0.10.28
* v0.10.27
* v0.10.26
* v0.10.25
* v0.10.24
* v0.10.23
* v0.10.22
* v0.10.21
* v0.10.20
* v0.10.19
* v0.10.18
* v0.10.17
* v0.10.16
* v0.10.15
* v0.10.14
* v0.10.13
* v0.10.12
* v0.10.11
* v0.10.10
* v0.10.9
* v0.10.8
* v0.10.7
* v0.10.6
* v0.10.5
* v0.10.4
* v0.10.3
* v0.10.2
* v0.10.1
* v0.10.0
* v0.9.12
* v0.9.11
* v0.9.10
* v0.9.9
* v0.9.8
* v0.9.7
* v0.9.6
* v0.9.5
* v0.9.4
* v0.9.3
* v0.9.2
* v0.9.1
* v0.9.0
* v0.8.28
* v0.8.27
* v0.8.26
* v0.8.25
* v0.8.24
* v0.8.23
* v0.8.22
* v0.8.21
* v0.8.20
* v0.8.19
* v0.8.18
* v0.8.17
* v0.8.16
* v0.8.15
* v0.8.14
* v0.8.13
* v0.8.12
* v0.8.11
* v0.8.10
* v0.8.9
* v0.8.8
* v0.8.7
* v0.8.6
* v0.8.5
* v0.8.4
* v0.8.3
* v0.8.2

Within joyent/node, development is currently focused on the `master`, `v0.10` and `v0.12` branches. `v0.10` is a long term support maintenance branch. `0.12` is the most recent release maintenance branch and `master` is the target for new development intended for `v0.13`

Current github statistics show that the joyent/node repository has 10,604 commits, 135 total branches, 254 releases, and 597 contributors.

### io.js

#### Organization

The github.com/iojs organization was established to support the io.js project.

The organization currently contains 282 members (https://github.com/orgs/iojs/people). There are 54 teams. (https://github.com/orgs/iojs/teams)

Teams:

* addon-api
* Bots
* build
* Collaborators
* Community-Members
* Core
* crypto
* docker
* docker-admin
* evangelism
* hardware
* iojs-ar
* iojs-bg
* iojs-bn
* iojs-cn
* iojs-cs
* iojs-da
* iojs-de
* iojs-el
* iojs-es
* iojs-fa
* iojs-fi
* iojs-fr
* iojs-he
* iojs-hi
* iojs-hu
* iojs-id
* iojs-it
* iojs-ja
* iojs-ka
* iojs-ko
* iojs-mk
* iojs-ms
* iojs-nl
* iojs-no
* iojs-pl
* iojs-pt
* iojs-ro
* iojs-ru
* iojs-sv
* iojs-ta
* iojs-tr
* iojs-tw
* iojs-uk
* iojs-vi
* platform-arm
* platform-freebsd
* platform-solaris
* platform-windows
* Streams
* Supports
* TC
* Tracing
* Website

#### Repositories

The current repositories within the io.js organization include:

* io.js
* roadmap
* build
* nan
* website
* evangelism
* docker-iojs
* readable-stream
* LTS
* hardware
* tracing-wg
* NG
* node-addon-examples
* doc-tool
* build-containers
* build-container-sync
* logos
* iojs-ro
* iojs-bn
* iojs-de
* iojs-nl
* iojs-da
* iojs-mk
* iojs-cs
* iojs-sv
* iojs-bg
* iojs-hi
* iojs-tw
* iojs-ko
* iojs-es
* iojs-pl
* iojs-id
* iojs-vi
* iojs-ja
* iojs-tr
* iojs-cn
* iojs-ru
* iojs-fr
* iojs-hu
* iojs-pt
* iojs-uk
* iojs-ka
* iojs-fi
* iojs-fa
* iojs-ta
* iojs-it
* iojs-no
* iojs-el
* iojs-ms
* iojs-ar
* iojs-he

#### iojs/io.js Branches and Tags:

Branches:

* master
* mergev010/base
* mergev010/cp-fixes
* more-working-groups
* next
* old-master
* only-consensus-seeking
* roadmap
* try
* v0.10
* v0.12
* v1.8.0-commit
* v1.x
* vupdates
* working-groups

Tags:

* v1.8.1
* v1.7.1
* v1.7.0
* v1.6.4
* v1.6.3
* v1.6.2
* v1.6.1
* v1.6.0
* v1.5.1
* v1.5.0
* v1.4.3
* v1.4.2
* v1.4.1
* v1.3.0
* v1.2.0
* v1.1.0
* v1.0.4
* v1.0.3
* v1.0.2-release
* v1.0.2
* v1.0.1-release
* v1.0.1
* v1.0.0-release
* v1.0.0

Within iojs/io.js, development is currently focused on `master` and `v1.x`.

Current statistics show 11,369 commits (which include some overlap with joyent/node from the fork), 15 branches, 24 releases and 678 contributors.

### Converging the Organizations

1. Ownership of the current `github.org/iojs` organization will transfer to the Node.js Foundation.
2. The Organization will be renamed from "io.js" to "Node.js Foundation". Note that renaming of the organization will cause the URL for the org to change. Github's infrastructure automatically handles the redirection. For the sake of this document, `github.com/nodejs-foundation` is assumed.
3. The Owners of the Github Node.js Foundation Organization will include:
  * The existing joyent node-coreteam members.
  * The existing iojs TC members.
  * Additional supporting staff selected by the Foundation Board.
4. All members of the existing node-coreteam will be added as Collaborators within the organization.
5. A team representing the TSC members will be created (if one does not already exist). The membership of this team will be all current voting members of both the node-coreteam and io.js TC.
6. Ownership of the following joyent/* repositories will be transferred to the Node.js Foundation organization:
  * http://github.com/joyent/node
  * http://github.com/joyent/node-website
  * http://github.com/joyent/node-advisory-board
  * http://github.com/joyent/http-parser
  * http://github.com/joyent/docker-node
  * http://github.com/joyent/node-tracing (not clear if this one needs to move)
7. A new repository will be created called `nodejs-foundation/node.js`. This repository will become the converged project repository. The existing `nodejs-foundation/node` and `nodejs-foundation/io.js` repositories would continue in parallel to support each distinct release line.

Note: Step 6 might be optional. There may not be need to physically move those existing repositories under the Foundation organization. The decision will be made during the actual merge process.

## Converging the Projects

Once the organization merge has been completed, the `nodejs-foundation/node` and `nodejs-foundation/io.js` repositories would need to be systematically merged into a single `nodejs-foundation/node.js` repository. This task will be nontrivial and may be controversial.

To level set, there should be a basic ground rule: *All* features and capabilities currently supported by the current releases of both projects should be merged with no regressions, even if there are initial questions or disagreements over the current implementation of those items.

Areas of potential disagreement should be identified *before* the merge so that compromise resolutions can be found either in advance or during the merge process. Changes to specific implementation details of existing features might be necessary but *as a general rule*, there should be no loss of functionality between the two projects. If something worked pre-merge in either Node.js or io.js, it should continue to work post-merge.

### Merge Process

Of the two existing repositories, `iojs/io.js` has been the most active since the fork. Since that time, there has been some cherry-picking of commits between the two projects but the activity has been inconsistent and the separate code bases have diverged in fairly significant ways. Based on the commit history, the easiest merge approach will be to create the new `nodejs-foundation/node.js` repository as a Fork of the existing `iojs/io.js` (`nodejs-foundation/io.js`) repository, then cherry pick commits from `joyent/node` (`nodejs-foundation/node`) to merge in. Unfortunately, this will not be as easy as simply using `git format-patch` and `git am`.

The commits generally fall into three categories:

* Features
* Fixes
* Doc & Test

Feature commits will most likely need to be reimplemented using the original commit as a guide. There are some that may be able to transfer directly but they are likely rare.

Fix commits are tricky because, in many cases, the issue may have already been fixed in io.js but in a different way than what was landed in joyent/node. For these, the process is:

1. determine if there is an existing test case for the fix and if there is not, create one,
2. test to see if the issue has already been fixed in the io.js base,
3. if it has, compare the two fixes and determine if there were any additional pieces added to the `joyent/node` fix that need to be added
4. if it has not been fixed, port the fix from `joyent/node`

Doc & Test commits are handled in generally the same way as Fix commits.

#### Merging from Parallel io.js and node.js tracks

While the repositories are being merged, the existing io.js and node release streams will continue to operate. This implies that there will be new commits to both that will also need to be merged into the converged repo. Those are to be handled in generally the same way as the other commits.

Once the Foundation launches, the decision making process for both release streams follows the Foundation TSC guidelines with the combined TSC overseeing both individual release lines. That said, the TSC can delegate the day-to-day details of managing each release line to the existing individual project TCs.

While work is being done to converge the two lines, care must be taken when landing features or fixes in either line that would impact or conflict with changes being made in the other line. The goal is to avoid a situation where the release lines diverge further *after* the Foundation launch while effort is being made to bring the lines together. When significant changes come in that can have an impact on the larger effort, those should be reviewed by the combined TSC.

#### Exit Criteria

The converged repository will become the main repository for Node.js releases as soon as the TSC determines that the merger of the two projects is: (a) complete and (b) passes all tests demonstrating that the `master` is production ready. At this point, the `nodejs-foundation/io.js` and `nodejs-foundation/node` repositories move into maintenance mode only to support LTS of the prior release lines.

### Build and CI Environment

Node.js and io.js each currently use separate build and CI environments that will need to be merged. Given that this is a fairly specialized task that will require coordination with multiple parties and knowledge of specific platforms, the specific steps involved with merging the environments will be delegated to the Build Working Group which will be expanded to consist of members from both existing projects.

#### Node.js Jenkins

The Node.js Jenkins environment is hosted at http://jenkins.nodejs.org and is managed by Joyent. It is currently on Jenkins version 1.590.

There are currently 14 nodes including the master. These cover:

* centos-5.7
* freebsd9.1
* master
* osx-build
* osx-home
* smartos-base-13.3.1
* smartos-base-13.4.0
* smartos-nodejs.org
* ubuntu-10.04
* ubuntu-12.04
* ubuntu-14.04
* windows-2k12
* windows-2k8r2
* windows-azure

Based on the configuration information available within Jenkins, it is not clear exactly where these nodes are hosted and whether they are owned or provided assets.

#### io.js Jenkins

The io.js Jenkins environment is hosted at https://jenkins-iojs.nodesource.com and is managed by NodeSource. It is currently on Jenkins version 1.6.10.

There are currently 60 nodes including the master. These cover:

* iojs-digitalocean-centos5-32-1
* iojs-digitalocean-centos5-64-1
* iojs-digitalocean-centos5-gcc41-32-1
* iojs-digitalocean-centos5-gcc41-64-1
* iojs-digitalocean-centos5-release-32-1
* iojs-digitalocean-centos5-release-64-1
* iojs-digitalocean-centos6-64-1
* iojs-digitalocean-centos6-64-gcc44-1
* iojs-digitalocean-centos7-64-1
* iojs-digitalocean-containers-debian+stable-1
* iojs-digitalocean-containers-debian+stable-2
* iojs-digitalocean-containers-debian+testing-1
* iojs-digitalocean-containers-debian+testing-2
* iojs-digitalocean-containers-ubuntu+lucid-1
* iojs-digitalocean-containers-ubuntu+lucid-2
* iojs-digitalocean-containers-ubuntu+precise-1
* iojs-digitalocean-containers-ubuntu+precise-2
* iojs-digitalocean-containers-ubuntu+trusty-1
* iojs-digitalocean-containers-ubuntu+trusty-2
* iojs-digitalocean-fedora21-1
* iojs-digitalocean-ubuntu1004-32-1
* iojs-digitalocean-ubuntu1004-64-1
* iojs-digitalocean-ubuntu1204-64-1
* iojs-digitalocean-ubuntu1404-32-1
* iojs-digitalocean-ubuntu1404-64-1
* iojs-digitalocean-ubuntu1404-gyp-32-1
* iojs-digitalocean-ubuntu1404-gyp-64-1
* iojs-digitalocean-ubuntu1410-64-1
* iojs-digitalocean-ubuntu1504-64-1
* iojs-joyent-smartos14-32-1
* iojs-joyent-smartos14-64-1
* iojs-linaro-armv8-ubuntu1404
* iojs-nodesource-armv7-ubuntu1401
* iojs-nodesource-armv7-ubuntu1401-release
* iojs-nodesource-raspbian-wheezy-pi1-1
* iojs-nodesource-raspbian-wheezy-pi1-2
* iojs-nodesource-raspbian-wheezy-pi1p-1
* iojs-nodesource-raspbian-wheezy-pi2-1
* iojs-nodesource-raspbian-wheezy-pi2-2
* iojs-nodesource-raspbian-wheezy-pi2-3
* iojs-nodesource-raspbian-wheezy-pi2-4
* iojs-online_net-armv7-wheezy-1
* iojs-online_net-armv7-wheezy-2
* iojs-online_net-armv7-wheezy-release-1
* iojs-rackspace-debian8-64-1
* iojs-rackspace-win2008r2-1
* iojs-rackspace-win2008r2-2
* iojs-rackspace-win2008r2-release-1
* iojs-rackspace-win2008r2-release-2
* iojs-rackspace-win2012r2-1
* iojs-rackspace-win2012r2-2
* iojs-rackspace-win2012r2-msvs2015-1
* iojs-voxer-freebsd101-32-1
* iojs-voxer-freebsd101-64-1
* iojs-voxer-osx1010-1
* iojs-voxer-osx1010-2
* iojs-voxer-osx1010-release-pkg-1
* iojs-voxer-osx1010-release-pkg-2
* iojs-voxer-osx1010-release-tar-1
* master

The nodes are provided by multiple third parties including NodeSource, DigitalOcean, Rackspace, and others.

### Merging the CI environments

Because the `nodejs.org` domain will transfer ownership to the Node.js Foundation, and because there is an existing `jenkins.nodejs.org` domain, it makes sense to use that domain for the combined Jenkins environment. The Build Working Group will need to put together the plan for combining the two Jenkins environments into one, including determination of where the master will be hosted.

The existing nodes need to be catalogued and organized into donated or owned assets. A transition plan for build assets currently owned by Joyent needs to be put in place. Will Joyent continue to provide those assets for use by the foundation? Will they be donated or leased? Likewise for all existing build assets used by io.js. If the build assets are donated, with the current providers of those be willing to continue providing those assets to the Node.js Foundation? If so, new agreements likely need to be drawn up. If the assets are leased or purchased, will the ownership of those leases or assets be transferred to the Foundation? Will the Foundation need to allocate a certain budget for those assets, etc. These details will need to be worked out but, in the interim, it should be possible to use either of the existing Jenkins environments to ensure continuity.

## Issues

The existing `nodejs-foundation/io.js` and `nodejs-foundation/node` issue databases would continue to be maintained. A brand new `nodejs-foundation/node.js` issue database will be established with a "clean slate". The existing io.js approach to managing issues will be adopted with this new issues database.

## Website and Social Media

Ownership of the iojs.org and nodejs.org domains will transfer to the Node.js Foundation. The existing nodejs.org and iojs.org websites will be merged and managed by a Website Working Group chartered by the TSC with staff and management assistance provided by the Node.js Foundation.

Ownership of the existing @nodejs and @official_iojs Twitter handles, Google+ and Facebook accounts will transfer to the Node.js Foundation and will become the responsibility of the Evangelization Working Group with staff and management assistance provided by the Node.js Foundation.

Ownership of the existing @nodejs mail servers will transfer to the Node.js Foundation and will become the responsibility of the TSC with staff and management assistance provided by the Node.js Foundation.