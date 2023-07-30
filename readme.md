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

<img src="https://github.com/tvanerven/materialsfrontend/raw/main/eu_logo.png" width="64" height="47">This project has received funding from the European Union’s Horizon 2020 research and innovation programme under grant agreement No 101017536. The funding was awarded through the RDA (https://www.rd-alliance.org/) Open Call mechanism (https://eoscfuture-grants.eu/provider/research-data-alliance) based on evaluations of external, independent experts.

### Adding or changing terms

Terms are policies which users need to accept before being allowed to create a profile. These are individually tracked by users, and can be accepted by users upon signup/sign-in in case of an update.

These can be created manually as follows:

- Login to Amy
- Go to `https://amy.charminghat.nl/admin/consents/term`
- Add your term. This includes the text it should provide, as well as how it should be formatted on the various form.
- Save. For starters, the term is optional. In case you want to make it required, open the term you've just created, and update it to be required.
