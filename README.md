# angular best practices
How to run
1. npm install -g @angular/cli
2. npm start

Angular Best practices recommendations

1. Use angular-cli.
2. Prefer LIFT approach:
   - Locate code quickly;
   - Identify code in glance;
   - Flatten folder structure;
   - Try do not DRY.
3. Folder structure (Group feature first then, component first):<br />
   - App Module (root of the application)
   - Core Module (shared singelton services across multiply modules in app, angular create new service for each lazy loaded service, app level component for example navigation bar)
   - Shared Module (shared components, directives and pipes for example load spinner)
   - Feature Module (feature level components, directives, pipes, services)

4. One item per file (use multiply component for on big component)
5. File naming (use *.component, *.service, *.model)
6. Make file names and class names consistence

Code Style
1. Single Responsibility
2. Use small functions
3. Prefer Immutable state
4. Prefixing component selectors
5. Using separate CSS and template files
6. Decorating input and output properties
7. Delegating complex logic to services
8. Component member sequence
9. Implementing lifecycle hook interfaces
10. When to create components

Angular performance
1. Ahead-of-time compilation (Compile before deploy)
   when use angular-cli
   npm run build -- --prod

2. Lazy Loading
   declare in route loadChildren command

3. Size of the bundles<br />
   npm run build -- --prod --source-maps=true<br />
   then use the source map explorer<br />
   use explicit imports to avoid loading of full library<br />
   import { Observable } from 'rxjs/Observable';<br />
   import 'rxjs/add/operator/map';<br />

3. Use pure pipes
4. Use trackBy to re-render only items what was changed
5. Don't Lazy-Load the Default Route
