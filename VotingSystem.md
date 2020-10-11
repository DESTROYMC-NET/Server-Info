# Voting System
This outlines the voting system, and how I added colored names.

I first created a group on LuckPerms called "gold," which had a prefix that was just simply `&e`. I also added a suffix that was `&r` so the color wouldn't leak onto player messages.

## Chat Format
We need to format the chat correctly so the prefix and suffix works. I used ChatControl to do this, which has an option to chat the message format.
```
Message_Format: '<{pl_prefix}{player}{pl_suffix}> {message}'
```
This format will put the prefix `&e` before the player's name, so their name will be colored. I then added the suffix `&r` after their name so their message was just normal. A chat message would look like this:
```
<&ehyperdefined&r> hello!
```
This is exactly how I wanted the colored names to work, so this setup worked out perfectly.

## Giving the Color
Since the prefix is on the `gold` group, I have to give the `gold` group to players. This is where SuperbVote comes in. This plugin will give rewards for voting. This is my config for the reward system.
```
rewards:
  - if:
      group: gold
    commands:
    - lp user %player% parent addtemp gold 6hr accumulate
    - delaysend %player% &eThanks for voting again! Your gold name will expire in %luckperms_group_expiry_time_gold%.
  - if:
      default: true
    commands:
    - lp user %player% parent addtemp gold 6hr
    player-message: "&aThanks for voting!"
```
The first section checks if you are in the group already. If you are, just add 6 more hours to the expire time. If you do not have the group, it will put you into the group for 6 hours.

You may notice the `delaysend` command. This was a custom command to run 1 second after it is executed. LuckPerms didn't update your data instantly, so the text that shows when your group expires was wrong. The command waits 1 second so LuckPerms can update and show the correct time.

It was a decent system that worked. There probably was a much better way of doing it.
