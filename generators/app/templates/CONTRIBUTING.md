# Contributing to '<%= name %>'

## Support / Questions

For **support or usage questions** like "How do I do X with <%= name %>." and "My code doesn't work.", please search and ask on **StackOverflow** with a **'<%= name %>' tag** first.

## Bugs

**Before filing an issue please [search the issue tracker](https://github.com/<%= github %>/<%= name %>/issues); your issue may have already been discussed or fixed in `master`.**

**Fill in the template** provided by the issue tracker, try to be as **clear** and **complete** as possible, providing a **[Short, Self Contained, Correct (Compilable), Example (SSCE)](http://sscce.org/)** (**link** to a **repository**) helps a lot .

## Feature / Enhancement Requests

Feature or enhancement requests should be **submitted** in the
[issue tracker](https://github.com/<%= github %>/<%= name %>/issues), with a **description** (follow the template) of the expected behavior & use case, where they’ll remain until **approval** by the **lead maintainer(s) and/or enough interest** from the **community**.

You can **request** a feature by **writing a pull request**, but this is **no guarantee** it will be **merged**.


## Pull Requests (PR)

In general, the contribution workflow looks like this:

1. **Fork** the repo.
2. **Clone** the repo. `git clone https://github.com/your-username/<%= name %>.git`.
3. Create a **new branch** based off the master branch, provide a **descriptive name** <br/>(ex. '**feat**-add-better-logging', '**bug**-removed-double-method', '**enh**-bumped-eslint')
4. Before running the code you’ll need to **install** the **dependencies** (`npm install` or `yarn`).
5. **Implement** your feature / bugfix (using the **watch scripts**), you should **only need to modify `/src`**. Don’t worry about regenerating the build folders (`/cjs`, `/es`, `/dist`), they are **built** in the **prepublish** phase.
6. Make sure **all tests pass**, **coverage is 100%** and there are **no linting errors**.
7. Submit a **PR**, referencing what it addresses.
8. Please try to keep your **PR focused in scope and avoid including unrelated commits**<% if (gitmoji) { %>, use **[Gitmoji](https://gitmoji.carloscuesta.me/)** in your commits<% } %>.

After you have submitted your PR, we'll try to **get back to you as soon as possible**. <br/>We will **review** your PR and might **request changes**.

## Development / Watch mode

You can **run the watch scripts**

```console
npm run build:watch
```

and

```console
npm run test:watch
```

to make development easier.

## Coding Guidelines

Please **follow** the **conventions** already established in the code.

Guidelines are enforced using **[ESLint](http://eslint.org/)**.
<% if(flow){ %><br/>Code is typechecked via **[Flow](https://flowtype.org/)**<% } %>

You can **run the linting script** by using

```console
$ npm run lint
```
<% if(flow){ %>
**Add Flow types** where possible, try to aim for **100% flow covered files**.
<% } %>

## Testing

Include updated (or add new) tests in the `__tests__` directory as part of your PR.

You can **run the test script** by using

```console
$ npm run test
```

or with coverage

```console
$ npm run test:coverage
```

Aim for **100% [coverage](https://en.wikipedia.org/wiki/Code_coverage)**.

## Hooks

We added **pre-commit** and **pre-push** **hooks** to make sure you **don't commit non-working code.**