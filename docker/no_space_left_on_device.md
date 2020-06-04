<H3>Notes</H3>

For people running into No Space left on the device  running docker containers using Docker for mac. The following [link](https://djs55.github.io/jekyll/update/2017/11/27/docker-for-mac-disk-space.html) gives a good explanation of whats going on.
I was running into this issue every once in a while(w/o any clue what was happening) so I thought its probably worth sharing.
Series of events:
- Wasn’t able to run a pg docker container with seeded data(it would fail while loading the data) cuz of No space left ... error.
- Ran docker system prune -a(to free up some space for un-used images/containers/volumes)
- Tried running the same pg container. Worked for a day.
- Next day, I stopped the older pg container ran another one, only to be running into same no disk space error.
- Did docker system prune -a. Even though it freed up some space again(relatively less that before), it wasn’t able to run the Pg container again.
- Checked the Disk location size in the docker preferences, and it seemed to still use all of the ~60G of the disk image file. Refer to the screenshot attached. The screenshot isn’t entirely correct reflection of that, cuz I didn’t took the screenshot before. This is after I cleared it.
- As per the article, the docker system prune -a for some reason should have Triggered a TRIM command and should have freed the space down but for some reason it didn’t :manshrug:
- Had to manually delete the docker.raw file and restart docker. That reset the disk space currently used space to ~ 4GBs.
Note: Be careful with deleting docker.raw in case you have some of the volumes that you would probably need, cuz it might probably would get rid of those well(TBH I don’t know how that works so :manshrug:)

<H4>Followup:</H4>
Now for some reason, when I did system prune again this morning, it seemed to have cleared the sectors from the Docker.raw file, not sure why it didn’t happened the first time.
