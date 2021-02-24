# Unbound
This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 11.2.1.

## Development server
Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding
Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build
Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

1. `ng build --prod --base-href=/unbound/`
2. dist/unbound>> CLI>> `jar -cvf unbound.war *`
3. To deploy Apache Tomcat>>  
	i) add the tag`<Valve className="org.apache.catalina.valves.rewrite.RewriteValve" />` into the Host tag (`<Host name="localhost"  appBase="webapps"  unpackWARs="true" autoDeploy="true"> </Host>`) in conf/server.xml file.  
	ii) Create rewrite.config with these lines below:
	<pre>
	RewriteCond %{REQUEST_PATH} !-f
	# RewriteRule ^/unbound/(.*) unbound/index.html
	RewriteRule ^/unbound/hello unbound/index.html
	</pre>

## Running unit tests
Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests
Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help
To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.

## Markdown
https://github.com/emn178/markdown/blob/master/README.md
