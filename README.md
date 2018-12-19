## Mapbox iFrame Test

A simple harness to exercise running mapbox-gl-js in a "cross-iframe"
scenario, meaning that a copy of mapbox-gl-js loaded in one window is used
to manipulate DOM owned by another window (i.e. a child iframe).

### To use this harness:

1. Install a mapbox-gl-js dev environment from the instructions at
https://github.com/mapbox/mapbox-gl-js/blob/master/CONTRIBUTING.md

2. Cd into your mapbox-gl-js clone.

3. Build mapbox-gl-js with

```
> yarn run {your desired build}
> yarn run build-css
```

where {your desired build} is one of `build-prod-min`, `build-dev`, or `build-prod`. E.g.

```
> yarn run build-prod-min
> yarn run build-css
```

4. Create a top-level mapbox-dist/ directory in this project.

5. Copy the contents of your clone's dist/ directory to this project's mapbox-dist/ directory.

6. Set your mapbox access token in setAccessToken.js

7. In index.html, uncomment the `<script>` tag appropriate to the type of build you did
   in step 3.

8. Open index.html in a browser (over file:// or http:// protocols). Use the maps!
