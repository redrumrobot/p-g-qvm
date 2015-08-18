This feature allows for up to 10 seperate chat channels to be created in tremulous. These channels can be password protected, and can be registered by users.

## Join ##
To join/register a channel, simply type `/join` **<channel 0-9>** _(password)_

If a channel is registered, you will join it. If it isn't registered, you will register it.

Registration is different than you may think it is, be sure to read the notes on it later

## Part ##
To part a channel, simply type `/part` **<channel 0-9>**
If you are the only user in that channel, the registration will be dropped.

## Chatting ##
To chat to a channel, a user would type the following:
`/# message`
`#` is the number of the channel. A user must be in this channel to chat into it

If you run this command without a message, and are in the channel, it will tell you the password, as well as who is using that channel with the same password.

## !seen ##
!seen lets a user see when another user was last online in the server. This information is saved into `chat.dat`. A player must be registered on a server to appear in this listing. If you don't complete a name, it will show the first 10 names.

## Channel Registration and chat.dat files ##
Channel registration is complex, and information has to be stored into a seperate file. For ease of administration, chat channel information has been saved into a chat.dat file (the default, you can change it, see notes) if the user is registered. This file stores each user's registered channels and their passwords, as well as !seen information

## Notes ##
  * `g_chat` defines the chat.dat file, defaults to chat.dat
  * This feature is in early development, so may be buggy.
  * User passwords are stored plain text, so inform your users of this.
  * Channels must be rejoined on map change/restart