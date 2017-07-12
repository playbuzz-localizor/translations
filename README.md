# Translations
playbuzz-localizor is a repository that store all playbuzz platfor translations.

  - Create
  - Play

# POeditor
 is an online localization management tool, perfect for collaborative or crowdsourced translation projects. Translate websites, apps, games and more!
 Log in to playbuzz account using this github credentials.
[poeditor](https://poeditor.com/projects/)
# POeditor Integration
This repository use webhooks to sync terms and translations to POeditor

To import terms and translations from POeditor use the Jenkins tasks:
  -  [Poeditor-Creator-Translations-Export](https://jenkins.playbuzz.com/job/Poeditor-Creator-Translations-Export) - Creator translations.
  - [Poeditor-Play-Translations](https://jenkins.playbuzz.com/job/Poeditor-Play-Translations-Export/) - Play translations.

The Creator and Play projects sync his terms and translations with the develop branch.
After each deploy there is need to merge the develop branch to master .

# Add new language

  1. Add empty json file, and name it with the language locale code, to the relevant project in the 'translations' repository.
  2. Add new new language to the relevant project in POeditor.
  3. Configure the relevant Jenkins task to support the new language in the LANGUAGE property.
  4. Export the project terms to the empty json file by using the relevant jenkins task.

- When all terms are translated, to export the translations, run Jenkins task again.

