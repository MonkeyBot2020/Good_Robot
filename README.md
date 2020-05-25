<h2>Good_Robot</h2>
Good_Robot is a Python Discord bot designed to streamline server management and channel migration. Utility and admin bots are dime-a-dozen, so I made this with functions that I couldn't find in others. Do note that it is an ongoing work in progress. 

<br/>Current functions:
<li>Channel logging: makes logging messages off the channel a breeze</li>
<li>Channel migration assistant: assists in migrating channels from one server to another</li>
<li>Profanity filter (filter swear words): a basic filter to help protect your channel</li>
<li>Statistics: helpful stats about the server and members</li>
…and more, with new features added regularly!</br></br>
<blockquote>Good_Robot requires the <em>manage_messages</em> permission to apply profanity filter to the channel.</blockquote>
To migrate channels between servers, simply log the channel to a text file (using the <code>!log</code> command) and simply print it to the new channel using the <code>!print</code> command. Command parsing for this program was done using COMPARSE: a flexible commandline parsing module. Designed to pick out ATTRIBUTES and assign VALUES to them from a message containing many un-formatted attributes/variables.</br></br>

<em>General_Functions: </em></br>
!about - Info about this bot
!show_id - Shows the message author's id; alias: ['my_id', 'id']
!logout - Logs the bot out of the server (admin only!)

<em>Help: </em></br>
!help - This help menu

<em>Profanity_Filter: </em></br>
!toggle - Toggles profanity filter ON/OFF (admin only!); alias: ['toggle_filter']

<em>Recorder: </em></br>
!log - Logs the channel to a text file (files cached for 5 days). Options:
+ file_name: logs channel to file; default: 'logs.txt'
+ filter: filter log by content; default: 'None'
+ exclude: exclude content from log; default: 'None'
+ log_attachments: logs attachments; default: 'True'
+ log_author: logs message author; default: 'True'
+ limit: limits number of messages logged; if 'None', logs the entire channel; default: 'None'
+ from: obtains messages AFTER specified date
+ to: obtains messages BEFORE specified date

!print - Prints message attachment to channel. Options:
+ file_name: log file to printed to the channel; default: 'logs.txt'

<em>Statistics: </em></br>
!members - Displays member statistics; alias: ['member']
<br/>!show_stats - Displays server statistics over the last week; alias: ['statistics', 'show_stat']

<em>Example: </em></br>
<code>!log 'example.txt', content_filter 'apple', exclude_content 'pie, candy', log_attachments False, log_author True</code>
