<h2>Good_Robot</h2>
Good_Robot is a Discord bot written in Python. Utility and admin bots are dime-a-dozen, so I made this with functions that I couldn't find in others. Do note that it is an ongoing work in progress. Current functions:
<li>1. Channel logging: makes logging messages off the channel a breeze.</li>
<li>2. Channel migration assistant: assists in migrating channels from one server to another</li>
<li>3. Profanity filter (filter swear words): a basic filter to help protect your channel</li>
…and more, with new features added regularly!</br>

<blockquote>Good_Robot requires the <em>manage_messages</em> permission to apply profanity filter to the channel.</blockquote>
Command parsing for this program was done using COMPARSE: a flexible commandline parsing module. Designed to pick out ATTRIBUTES and assign VALUES to them from a message containing many un-formatted attributes/variables.

<em>Usage: </em>
<code>!log_this_channel 'logs.txt'</code>
<ul>
	<li>Logs the channel the administrator is currently in to a specified file. Note, only administrators may use this. USAGE: log_this_channel='logs.txt' See below for options.</li>
	<li>VARIABLE TYPE: str</li>
	<li>ALTERNATIVES: -!log_this_channel=LOG_THIS_CHANNEL, -!log_this_channel:LOG_THIS_CHANNEL, -!log_this_channel LOG_THIS_CHANNEL</li>
</ul>
<code>!log_this_channel, content_filter=None</code>
<ul>
	<li>OPTIONAL PARAMETER: Filter log by content. USAGE: !log_this_channel, content_filter=None</li>
	<li>VARIABLE TYPE: str</li>
	<li>ALTERNATIVES: -content_filter=CONTENT_FILTER, -content_filter:CONTENT_FILTER, -content_filter CONTENT_FILTER</li>
</ul>
<code>!log_this_channel, exclude_content=None</code>
<ul>
	<li>OPTIONAL PARAMETER: Exclude content from log.</li>
	<li>USAGE: !log_this_channel, exclude_content=None</li>
	<li>VARIABLE TYPE: str</li>
	<li>ALTERNATIVES: -exclude_content=EXCLUDE_CONTENT, -exclude_content:EXCLUDE_CONTENT, -exclude_content EXCLUDE_CONTENT</li>
</ul>
<code>!log_this_channel, log_attachments=True</code>
<ul>
	<li>OPTIONAL PARAMETER: Logs attachments.</li>
	<li>USAGE: !log_this_channel, log_attachments=True</li>
	<li>VARIABLE TYPE: bool</li>
	<li>ALTERNATIVES: -log_attachments=LOG_ATTACHMENTS, -log_attachments:LOG_ATTACHMENTS, -log_attachments LOG_ATTACHMENTS</li>
</ul>
<code>!log_this_channel, log_author=False</code>
<ul>
	<li>OPTIONAL PARAMETER: Logs author of message.</li>
	<li>USAGE: !log_this_channel, log_author=False</li>
	<li>VARIABLE TYPE: bool</li>
	<li>ALTERNATIVES: -log_author=LOG_AUTHOR, -log_author:LOG_AUTHOR, -log_author LOG_AUTHOR</li>
</ul>
<code>!print_to_channel 'logs.txt'</code>
<ul>
	<li>Print the message attachments to the channel the administrator is currently in. Note, only administrators may use this.</li>
	<li>USAGE: !print_to_channel</li>
	<li>VARIABLE TYPE: str</li>
	<li>ALTERNATIVES: -!print_to_channel=PRINT_TO_CHANNEL, -!print_to_channel:PRINT_TO_CHANNEL, -!print_to_channel PRINT_TO_CHANNEL</li>
</ul>
<code>!profanity_filter=False</code>
<ul>
	<li>Filters swear words and warns the offending user.</li>
	<li>USAGE: !profanity_filter=False</li>
	<li>VARIABLE TYPE: bool</li>
	<li>ALTERNATIVES: -!profanity_filter=PROFANITY_FILTER, -!profanity_filter:PROFANITY_FILTER, -!profanity_filter PROFANITY_FILTER</li>
</ul>
<blockquote>[if the value for the variable is not specified, then its specified default value is used]

<strong>optional arguments: --h, --help [show this help message and exit]</strong></blockquote>
<i>Example use:</i>
To log channel messages in 'example.txt', filtering only messages that contain 'apple', excluding 'pie' and 'candy', not log attachments while logging author names, one would type the following (Note: Good_Robot is not strict on syntax. Hence, you could pass "!log_this_channel example.txt" instead of "!log_this_channel='example.txt'"):

<code>!log_this_channel 'example.txt', content_filter 'apple', exclude_content 'pie, candy', log_attachments False, log_author True</code>
