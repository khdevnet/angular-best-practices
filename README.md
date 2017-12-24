# angular best practices
How to run
1. npm install -g @angular/cli
2. npm start

Angular Best practices recommendations

1. Use angular-cli
2. Prefer LIFT approach
   - Locate code quickly
   - Identify code in glance
   - Flatten folder structure
   - Try do not DRY
2. Folder structure (Group feature first then, component first)
   App Module,
   - Root of the application 
   Core Module,
   - shared singelton services (shared across multiply modules in app) angular create new service for each lazy loaded service
   - app level component (navigation bar)
   Shared Module, 
   - shared components, directives and pipes (load spinner)
   Feature Module
   - feature level components, directives, pipes, services

3. One item per file (use multiply component for on big component)
4. File naming (use *.component, *.service, *.model)
5. Make file names and class names consistence

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

Perfomance
1. Ahead-of-time compilation (Compile before deploy)
   when use angular-cli
   npm run build -- --prod

2. Lazy Loading
   declare in route loadChildren command

3. Size of the bundles
npm run build -- --prod --source-maps=true
then use the source map explorer
use explicit imports to avoid loading of full library
import { Observable } from 'rxjs/Observable';
import { Subject } from 'rxjs/Subject';
import 'rxjs/add/operator/map';
import 'rxjs/add/observable/empty';
import 'rxjs/add/operator/delay';

3. Use pure pipes