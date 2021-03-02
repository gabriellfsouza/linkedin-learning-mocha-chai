# Nadia’s Garden Restaurant

This is a Node.js and Express website that accepts and lists restaurant reservations. Improve it with the lynda.com course, "Node.js: Testing and Code Quality" by Jon Peck.

The backend contains intentional mistakes, like weak validation on email addresses. Inconsistencies in coding style are also intentional.

## Getting Started

```bash
npm install
npm start
```

The server runs on port 3000.

There are three routes:

- http://localhost:3000/ - homepage
- http://localhost:3000/reservations - submit a reservation booking request
- http://localhost:3000/admin - view all booking requests; basic auth login/password `admin`

The server persists using a SQLite3 database named `database.sqlite` in the site root.

## Development

This project uses EditorConfig to standardize text editor configuration.
Visit http://editorconfig.org for details.

This project uses ESLint to detect suspicious code in JavaScript files.
Visit http://eslint.org for details.

### Testing

This project uses Mocha and Chai for testing.
Visit http:mochajs.org and http://chaijs.com for details.

To execute tests:

```bash
npm test
```

### Debugging

This project uses https://www.npmjs.com/package/debug for development logging. To start `nodemon` and enable logging:

```bash
npm run debug
```

## FAQ

- Q: Why didn't you store the time submitted?
  - A: I wanted to reduce the number of fields and simplify testing.
- Q: Wouldn't it be easier if the form submitted a datetime string instead of building and parsing one?
  - A: Yes, it would, but the form logic is simpler. Either way, someone has to do the work.
- Q: Why did you mix a callback and a Promise in `lib/reservations.js`?
  - A: `Joi` doesn't support Promises, but it does support callbacks. I wanted to show how to test both kinds of asynchronous code.
- Q: How'd you handle cross-platform support?
  - A: Avoided relative directories, used `cross-env` to transform environmental variables.
