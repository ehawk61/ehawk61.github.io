+++
author = "Jonathan L Meek"
title = "Cleaning Up NixOS Profiles"
date = "2025-02-01"
description = "My discovery of cleaning up NixOS Profiles out of my GRUB Menu"
toc = false
tags = [
    "nixos",
    "how-to",
    "profiles",
    "grub"
]
+++
> Update 2025-02-07
> A few folks in my circle and [online](https://hachyderm.io/@j_l_meek/113931854758112151) pointed me to
> using `nix-collect-garbage -d` as a way to clean up my profiles. In my own personal testing, this works
> BUT I found it was flagging all my profiles. Also when I applied the `--delete-older-than` flag it was
> flagging things that were less than the timeframe. For example, I would set it for
> `--delete-older-than 30d` but it would have a profile that I created in the  past few days. Without
> digging too deep into things, I have a feeling that the flags are using a different date than my
> expectation. I was expecting the command to use the date of when I created the profile.
> I think going forward I will use the `nix-collect-garbage` command but I think the advice below is great
> for those who need more control in what gets purged. Again, I am still learning so I might find
> something better and happy to update.

In my adventures with NixOS, I got carried away in using profiles when I do `nixos-rebuild switch` for a system upgrade and/or adding new software to the laptop. I love idea of reverting when I screw something up without too much trouble. I had built up a collection about 40 items in my bootloader and realized I could do some pruning since they are there as "oh shit" catchers. However when I began looking around there wasn't clear advice on how to do this. I discovered a way to do this in case you pulled a me and overused the profile feature.


> Standard disclaimer: You are messing with the guts of your NixOS which require root access. While this
> worked for me, I also keep diligent backups of my data and snapshots of my OS so I could always revert
> or abandon and start over. The advice might backfire because you failed to backup prior hand. So stop
> reading, ensure you have backed up and TESTED your restores BEFORE you go any further.

Now that my moral obligation has been met, let's begin:

1. Backup you data
	- Seriously, I am giving you every chance to avoid calamity here
2. Test that you can recover from your backups
	- My personal favorite method is picking a random document and opening it up
3. If you are using ZFS, take a snapshot of your `/nix` directory
4. Navigate to your `/nix/var/nix/profiles/system-profiles`
5. You will notice that the items listed here match what you see in GRUB menu
6. Also there will be two entries:
	- `<profile name>`
	- `<profile name>-1-link`
7. Run `rm <insert profile name here>`
8. Run  `rm <insert profile name here>-1-link`
9. Run `nixos-rebuild boot`
10. Take a deep breath
11. Restart your computer
12. Upon restart, you will see that the entry is no longer in your GRUB listing

Great, you have a way to clear our profiles and not damage your system! Some things to note:
- Make sure that you don't blow away a profile you are actively logged into it or a profile that what you system defaults to on bootup
- Do this piecemeal, this is a prime space to footgun your way to victory
- Did I mention backups and doing a test restore from said backups before doing this?
    - Yep, I did. Three times. Cool. The hosts of 2.5 admins would be proud.

Feel free to drop me feedback on [mastodon](https://hachyderm.io/@j_l_meek) if you found this helpful or see something I didn't quite get right.



