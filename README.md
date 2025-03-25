# historic-results
This is a template repo for an open archive for capturing the history of the sport in a crowdsourced manner.

For the moment, it's just a README with an overview of the idea.  If other like the idea, I'd move the repo
into the `openathletics` GitHub organisation, and try to set up the environments.

The rough scope in mind...
1. Allow anyone to upload old results and heritage materials (e.g. PDF and scans) into a safe location, tagging things at the time to give some clues about what they relate to (e.g. year, location, competition name)
2. Use OCR tools to turn these into structured textual data
3. Experiment with parsers and machine-learning code to recognize  and normalize into recognisable results - e.g. races/events with bibs, places, times, athlete names
4. Match and import into a growing database of competitions/events/results, organisations, people and places. 

Once there, the "fun part" would be to allow fans to annotate, correct and link to the archive; upload or link photos of a competition; analyse and visualize in interesting ways etc.  Any developer in principle could pull down and set up a copy, and offer a contribution.

## Why Historic Results?
This is a deliberate choice as it's a common need or desire,  but clearly non-commercial. Service providers and data providers work to provide services "now", with information on currently-competing athletes; and there are commercial and privacy considerations.    But if we are dealing with (say) pre-2000 results, everyone referred to is an adult, and we don't have to store their contact details.

Meanwhile, every country has people keeping the history of their club or federation, and just wants a safe place to put it.
All data would be Open Data (e.g. Open Database Licence, like Wikipedia); all code would be open source.
We'd deliberately limit the data to avoid fields which go beyond the goal of the site.

This could also be a tesbed for many ideas discussed at past AthTech conferences. 
There are 


## Technical tools and design
OpenTrack could potentially provide some resources, if it's the "tools we know".  This would most likely be the following stack, which is reasonably mainstream

- Python language (3.13?), Django framework (5.2?)
- [apppack](https://apppack.io) framework to deploy onto AWS with best practices
- Social logins with e.g. django-allauth
- S3 bucket for large cheap storage
- Database (Postgres?) to manage users, logins, and structured data
- test environment always available, either ongoing or as temporary "review apps"
- a script to quickly pull down all assets and set up a local copy for development
- freedom to use any front end framework (JS/CSS) - we're agnostic, but Bootstrap is usually a good start
- whitenoise to compress/verify 

We could set this up quite quickly as an app that "does very little yet", but has all the above elements

## Initial content
There are a number of bodies such as Achilles Club who has 100+ years of archive materials, and Oxford Uni Cross Country Club where we already have a digitised 100-year set of results.  The file storage would be organised into folders based on country, then organisation, then their own files.

A data model would be a cut-down but similarly structured set of tables similar to OpenTRack's database.  We can set up regular exports of organisations/clubs
It's also possible that some national databases and statisticians may be willing to share and export structured data.

## Who might get involved
We're hoping to find a mixture of 
- technical people either working in athletics, or with hobby-time and skills, who want to collaborate and innovate
- IT students who are looking to work on projects for experience, 
- hopefully, in due course, their supervisors!
- statisticians who want to keep their archives safe
  
## How to get involved
Discuss at https://forum.openathletics.net/

