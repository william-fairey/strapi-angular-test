# Strapi4

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 13.3.2.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.

https://docs.strapi.io/developer-docs/latest/developer-resources/database-apis-reference/rest-api.html

apiUrl = http://strapiportal.promaster.com:1337/

Strapi API Endpoints

To retrieve a json list of articles
GET
/api/articles/

To retrieve a json article
GET
/api/articles/3

To add a like to an article
PUT
/api/articles/3

{
  "data": {
    "likes": "10"
  }
}

To add acomment
POST
/api/comments/

{
	"data": {
		"comment": "This is a reply to the comment",
		"name": "My Name",
		"email": "my@email2.add",
		"date": "2022-04-14T16:24:03.969Z",
        "articleId": 3,
        "commentParent": 4
	}
}

To retrieve Comments
GET
/api/comments/?filters[articleId][$eq]=3
/api/comments/?filters[articleId][$eq]=3&filters[commentParent][$eq]=4
