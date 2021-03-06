# Demo: Search breweries

Created by Kris Bastiani.

Made possible through the use of the [Open Brewery DB API](https://www.openbrewerydb.org/).

A simple UI that will live update a list of results based on the search query as long as it is at least 3 characters long.

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

## Limitations & areas for improvement

I haven't implemented any testing, nor proper linting standards beyond what came from `vue-cli`. Usually I would give these much higher priority, however I've prioritised as I would for a rapid prototype- i.e, just focus on getting something done that works.

While it doesn't prevent subsequent requests, stale requests are not being aborted currently. This would probably be my highest priority to address with more time, and I would likely do so through the use of JavaScript's [AbortController](https://developer.mozilla.org/en-US/docs/Web/API/AbortController). This should eliminate the potential need to queue requests to prevent them completing out of order.

The other improvement I'd ideally make given more time would be to throttle requests so that they're not firing on every keystroke- obviouosly throttling is what's sensible here and not debouncing as we'd need to make sure the final keystroke always fires.
