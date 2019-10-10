# Gentics Mesh MuseTech Example

This repository contains all the sources that were needed to build the [musetech.getmesh.io](https://musetech.getmesh.io) demo site.

## Blogpost

This demo project is covered by two blogposts:

* Musetech: TODO LINK
* Technical: TODO LINK

## Project structure

This project consists of two parts. The __importer__ contains the *schema models*, *contents* and is responsible of importing the *images*, *videos*, *audioguides*, *exhibits*, *pages* into the headless CMS.
The __app__ contains the front-end react app which will present the content in various formats to clients.

### Importer

The importer is a Java program which will setup the project in Gentics Mesh.

The _ImportRunner.java_ class contains the main runner which can be executed to run the importer.

The importer is using the [Gentics Mesh Java Client](https://getmesh.io/docs/platforms/#_clients) and [RxJava](https://github.com/ReactiveX/RxJava) to create the project, schemas, microschemas and nodes.

### App

The React front-end uses [CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) to access the Headless CMS API to fetch the contents via GraphQL. The URL for the Gentics Mesh instance that will be used can be configured in the `app/src/config.json` file.

The project can be build using `yarn && yarn build` or run via `yarn && yarn start`.

## Used software

* Backend: [Gentics Mesh - Headless CMS](https://getmesh.io)
* Frontend: [React](https://reactjs.org/), [Theme](https://blackrockdigital.github.io/startbootstrap-agency/)

## Contents

The contents that were used in this project have different licenses. The licenses have been added in the _json_ files. Please check the matching license before re-using the contents.

* Image: [Source List](importer/data/image/images.json)
* Video: [Source List](importer/data/video/videos.json)
* Text: All texts and descriptions are 
* Audio: The audio guides that are part of this project have been generated using the text source.

## TODO

* links, license for texts
* Review rights

## Ideas

* Add fake ticket shop connection
* Add showcase video which highlights features of the demo (e.g. show screen usage)
* Add reminders
* Add tour information
* Add current event info
* Highlight exhibits in screen view
* Mark specific exhibits to be shown in the screen
* Add gallery support for exhibit views
* Add paging to exhibit list view
* Add dedicated TLD
* Add fake screen image frame to screen list view (to better grasp the concept of the screens)
* Add login and admin area to better divide the website features
* Add information about current delays
* Add draft/publish handling
