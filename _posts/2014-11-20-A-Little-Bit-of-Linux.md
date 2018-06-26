---
layout: post
title: A Little Bit of Linux
tags: linux synology backup
---

Our company recently bought a [Synology DS412+](https://www.synology.com/en-us/support/download/DS412+) to use as network storage. I finally get a chance to see what so many people have been raving about. For such a (relatively) inexpensive device, this NAS is capable of quite a bit. What sets these units apart from other NAS units is the DiskStation Manager (DSM). Synology has really done a nice job with this operating system.

I have been setting up GitHub Enterprise in our office. I decided to install GitHub’s backup tools on the Synology and use one of the storage volumes for the backups. Doing this meant going to the Linux command-line on the Synology. As this was the second task I needed to run on the Synology that involved going to the command-line, I wasn’t completely fumbling my way around like I was the first time.

Getting the backup-tools installed and running was relatively painless. Making a successful backup, however, was not quite as easy. Now, I’m sure this wouldn’t have been much of an issue with someone more knowledgeable with Linux, but for me, it was a learning experience.

I kept getting `env: bash: No such file or directory` when it got to the point where it was backing up the repositories. I started looking through the backup scripts, but I couldn’t determine which script was failing until I added `set -x` to the main script. I then found the particular script that was failing.

After then discovering that DSM comes with the Ash shell and not Bash, I then knew to change `#!/usr/bin/env bash` to `#!/usr/bin/env ash`. Voila! Our GitHub repositories are now being backed up to the Synology every night. Now, time to figure out what to use for offsite backup of the Synology. Fun times!
