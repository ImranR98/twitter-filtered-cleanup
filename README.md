# Twitter Filtered Cleanup

Script to delete tweets, retweets, and likes that contain text that match any string from a user-defined list (case insensitive). This is done using the Twitter API and an account data archive you can [request from Twitter](https://twitter.com/settings/your_twitter_data).

## Requirements

1. A Python environment with the `tweepy` package installed.
2. A Twitter developer account with a new App created.
3. Twitter App and account credentials.
4. A Twitter data archive from your account, extracted to a directory.

## Usage

2 commands are available:
- `target` - This uses your twitter data archive and a provided list of strings to generate a list of Tweets to delete/un-like, which is saved in a directory you specify. The output file path is printed to `stdout`.
- `delete` - This uses a target Tweets file generated by the `target` command, along with Twitter credentials you provide, to delete/un-like the appropriate tweets.

Command syntax:
```text
Usage: python twitter-filtered-cleanup.py target [Twitter export directory] [target file destination directory] [filter string 1] [filter string 2] [filter string 3] ...
       python twitter-filtered-cleanup.py delete [target file path] [Twitter App API key] [Twitter App API secret] [Twitter App account access key] [Twitter App account access secret]
```

Note: `credentials.txt` is ignored by Git to allow for convenient credential storage.