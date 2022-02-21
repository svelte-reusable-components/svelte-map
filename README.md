# svelte-map

The map component implements a leaflet map, including a marker (and an optional "my location" button) for snel projects. (Snel is a cybernetical compiler for svelte applications in deno)

![image](https://user-images.githubusercontent.com/79450010/151322612-86ded8f5-b05c-406a-87bd-f3ec15d89623.png)

In case you have not created a snel project before, head to https://deno.land/x/snel@v0.6.0 and follow the steps to create one.

To then use it, import the link "https://deno.land/x/svelte_map/Maps.svelte" as shown in the usage example.

After you initiated a snel project and added the code shown below, you are able to see the component when running the project with "trex run start".

## Usage Example

Import the component and set longitude and latitude for the Marker.

```javascript
 import Map from "https://deno.land/x/svelte_map/Maps.svelte"
 
 let long = 50;
 let lat = 50;
```

Use the component in your code. Set long and lat and the button equal to {true} or {false} depending on whether the "My Location" button should appear.

```html
<Map long={long} lat={lat} button={true} />
```

### Change Map Center
```html
<Map bind:this={svelteMap} />
```

```javascript
let svelteMap
svelteMap.setMapCenter({
    lat: 30.08,
    long: -97.14,
})
```
