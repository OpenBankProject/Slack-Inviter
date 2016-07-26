Slack Invite Automation
------------

This is a tiny web application which would invite a user into Open Bank Project slack channel.

Originally forked from [Slack Invite Automotion Project](https://github.com/outsideris/slack-invite-automation) - Credits goes to [Outsideris](https://github.com/outsideris) for all the good stuff). Then forked again from our employee [Ismail](https://github.com/ichaib) for deployment on our server.

The Open Bank Project is an open source API for banks that enables account holders to interact with their bank using a wider range of applications and services. More info on www.openbankproject.com 


## Configuration

You need to drop following code into a file `config.js` and edit accordingly:

	module.exports = {
	  // your community or team name to display on join page.
	  community: process.env.COMMUNITY_NAME || 'YOUR-TEAM-NAME',
	  // your slack team url (ex: socketio.slack.com)
	 slackUrl: process.env.SLACK_URL || 'YOUR-TEAM.slack.com',
	  // access token of slack
	  // You can generate it in https://api.slack.com/web#auth
	  // You should generate the token in admin user, not owner.
	  // If you generate the token in owner user, missing_scope error will be occurred.
	  //
	  // You can test your token via curl:
	  //   curl -X POST 'https://YOUR-SLACK-TEAM.slack.com/api/users.admin.invite' \
	  //   --data 'email=EMAIL&token=TOKEN&set_active=true' \
	  //   --compressed
	  slacktoken: process.env.SLACK_TOKEN || 'YOUR-ACCESS-TOKEN',
	  // an optional security measure - if it is set, then that token will be required to get invited.
	  inviteToken: process.env.INVITE_TOKEN || null,
	
	  locale: process.env.LOCALE || "en",
	};
