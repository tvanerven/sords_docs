# Documentation project

This project contains a couple of handholds for the Django Admin for Amy, and where certain objects may be created.

## Logging in

Logging in is simple:

1. Go to [https://amy.charminghat.nl](https://amy.charminghat.nl)
2. Log in with the credentials you were given. If you don't have any credentials, get someone with permissions to add a Person to the platform.
3. Next, select Django Admin from the right top corner of the page. Alternatively go to [https://amy.charminghat.nl/admin/](admin) via the link.

You're now at the Django admin.

## Modifying objects

The Django admin is an interface which allows you to change instances of models. You can add, delete, and modify existing models that become visible in the webinterface.

Most of Amy is designed to offer this functionality, so you will only visit this interface in case you need to do specific things. These specific things are documented here.

### Email contents and triggers

Emails contain two moving parts: the email being sent and the trigger which sends the email.

Changing the email can be done under Autoemails/Email templates. You'll see a preview option there as well. 

Take care when modifying the parts of the email listed in `{{ this }}` format. These are internal template tags; only touch these if you know what you're doing.

Triggers are contained under Autoemails/Triggers. The triggers and their sending are fairly self-descriptive; a certain Action occurs, and as a result, a certain email is sent. You can modify the triggers to send a different email, but you can't add new ones without code changes.

### Changing curriculum

Changing curriculums can be done under Workshops/Curricula section. You can update the following fields:

- The ID (or shortname). This is represented at new Events.
- The name (or full name). This is represented on most pages with full text.
- The description; this can be used to build pages.
- The carpentry which it's linked to. You can't add new carpentries; this requires code changes.

You can also add a new curriculum by the top right button marked "add curriculum"

### Changing badges

Badges represent an accomplishment made by a student (or Person). To add a new badge, go to Workshops/Badges and select the New Badge button in the top right.

You can also modify existing badges.

### Changing tags

Tags are a shortname which can be connected to an event to indicate some metadata or status. A number of default tags are provided; you can add more via Workshops/Tags. 

Once you add a tag and save, it only becomes available to select. 

