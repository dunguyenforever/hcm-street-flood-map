# Ho Chi Minh City Street Flood Map
## Why was this project made?
Every year during the monsoon season in Ho Chi Minh City, Vietnam, the combination of heavy rainfall and insufficient urban infrastructure leads to severe flooding. This poses significant challenges for residents, including dangerous commutes and damaged vehicles. As an active commuter, I have experienced firsthand the chaos and dangers of navigating flooded streets. To address this problem, I designed a flood mapping system that provides real-time information on flood levels along specific routes, helping users avoid hazards and travel more safely during the monsoon season.
## Affordances
- Physical Affordances: An intuitive interface that allows users to interact with a map, visualize flood levels, and select safe routes easily.
- Cognitive Affordances: Clear visual indicators, such as color-coded flood levels, help users understand the severity of flooding at a glance.
- Functional Affordances: The ability to predict and display flooded areas in real-time, providing actionable insights to users.
## User Needs and Design Requirements
### User Needs 
- Real-time flood information for safer route planning.
- An intuitive and accessible interface that works on mobile and desktop devices.
- Accurate and reliable data about flood levels to minimize risks during commutes.
### Design Requirements
- A responsive user interface that integrates with live data sources to display real-time flood conditions.
- Visual elements, such as maps and icons, to represent road conditions clearly.
- Intelligent data analysis on the data of rain and high tide to predict flooding and display historical data.
## Designs and Sketches of the HCM Street Flood Map
The design features:
1. A map with real-time flood indicators using color-coded markers (e.g., green for safe, yellow for moderate, red for severe flooding).
2. A search bar for route planning.
3. Overlays showing flood intensity and safe alternate routes.
4. A dashboard summarizing key data like affected areas and travel tips.
![Screenshot 2024-12-09 030724](https://github.com/user-attachments/assets/6163712b-298e-4f99-b6b2-f83e710f5ba1)

## Implementation

### Features
- Real-time Flood Mapping: Displays flooded areas and their severity levels.
- Route Planning: Suggests alternative safe routes for commuters.
- Notifications: Sends alerts about worsening conditions in nearby areas.
- Intelligent display of the user's vehicle information and the flooding level to suggest safer travel.

## Future 
- Expand coverage by including more streets and information
- Expand functionality: including information on the roads and streets so it can be used in other weather conditions.
- Expand to mobile app and other format.
- Reactive and increase website's performance and flow for prettier and easier viewing of the information. 

## Use of AI 
- Suggestion on how to implement the external API
- Debugging on the styling of the website
  
## Libraries
Frontend: Mapbox API (for interactive maps), Svelte, HTML, JavaScript, CSS

# TO RUN LOCALLY
# Svelte + Vite

This template should help get you started developing with Svelte in Vite.

## Recommended IDE Setup

[VS Code](https://code.visualstudio.com/) + [Svelte](https://marketplace.visualstudio.com/items?itemName=svelte.svelte-vscode).

## Need an official Svelte framework?

Check out [SvelteKit](https://github.com/sveltejs/kit#readme), which is also powered by Vite. Deploy anywhere with its serverless-first approach and adapt to various platforms, with out of the box support for TypeScript, SCSS, and Less, and easily-added support for mdsvex, GraphQL, PostCSS, Tailwind CSS, and more.

## Technical considerations

**Why use this over SvelteKit?**

- It brings its own routing solution which might not be preferable for some users.
- It is first and foremost a framework that just happens to use Vite under the hood, not a Vite app.

This template contains as little as possible to get started with Vite + Svelte, while taking into account the developer experience with regards to HMR and intellisense. It demonstrates capabilities on par with the other `create-vite` templates and is a good starting point for beginners dipping their toes into a Vite + Svelte project.

Should you later need the extended capabilities and extensibility provided by SvelteKit, the template has been structured similarly to SvelteKit so that it is easy to migrate.

**Why `global.d.ts` instead of `compilerOptions.types` inside `jsconfig.json` or `tsconfig.json`?**

Setting `compilerOptions.types` shuts out all other types not explicitly listed in the configuration. Using triple-slash references keeps the default TypeScript setting of accepting type information from the entire workspace, while also adding `svelte` and `vite/client` type information.

**Why include `.vscode/extensions.json`?**

Other templates indirectly recommend extensions via the README, but this file allows VS Code to prompt the user to install the recommended extension upon opening the project.

**Why enable `checkJs` in the JS template?**

It is likely that most cases of changing variable types in runtime are likely to be accidental, rather than deliberate. This provides advanced typechecking out of the box. Should you like to take advantage of the dynamically-typed nature of JavaScript, it is trivial to change the configuration.

**Why is HMR not preserving my local component state?**

HMR state preservation comes with a number of gotchas! It has been disabled by default in both `svelte-hmr` and `@sveltejs/vite-plugin-svelte` due to its often surprising behavior. You can read the details [here](https://github.com/sveltejs/svelte-hmr/tree/master/packages/svelte-hmr#preservation-of-local-state).

If you have state that's important to retain within a component, consider creating an external store which would not be replaced by HMR.

```js
// store.js
// An extremely simple external store
import { writable } from 'svelte/store'
export default writable(0)
```


# Svelte + Vite

This template should help get you started developing with Svelte in Vite.

## Recommended IDE Setup

[VS Code](https://code.visualstudio.com/) + [Svelte](https://marketplace.visualstudio.com/items?itemName=svelte.svelte-vscode).

## Need an official Svelte framework?

Check out [SvelteKit](https://github.com/sveltejs/kit#readme), which is also powered by Vite. Deploy anywhere with its serverless-first approach and adapt to various platforms, with out of the box support for TypeScript, SCSS, and Less, and easily-added support for mdsvex, GraphQL, PostCSS, Tailwind CSS, and more.

## Technical considerations

**Why use this over SvelteKit?**

- It brings its own routing solution which might not be preferable for some users.
- It is first and foremost a framework that just happens to use Vite under the hood, not a Vite app.

This template contains as little as possible to get started with Vite + Svelte, while taking into account the developer experience with regards to HMR and intellisense. It demonstrates capabilities on par with the other `create-vite` templates and is a good starting point for beginners dipping their toes into a Vite + Svelte project.

Should you later need the extended capabilities and extensibility provided by SvelteKit, the template has been structured similarly to SvelteKit so that it is easy to migrate.

**Why `global.d.ts` instead of `compilerOptions.types` inside `jsconfig.json` or `tsconfig.json`?**

Setting `compilerOptions.types` shuts out all other types not explicitly listed in the configuration. Using triple-slash references keeps the default TypeScript setting of accepting type information from the entire workspace, while also adding `svelte` and `vite/client` type information.

**Why include `.vscode/extensions.json`?**

Other templates indirectly recommend extensions via the README, but this file allows VS Code to prompt the user to install the recommended extension upon opening the project.

**Why enable `checkJs` in the JS template?**

It is likely that most cases of changing variable types in runtime are likely to be accidental, rather than deliberate. This provides advanced typechecking out of the box. Should you like to take advantage of the dynamically-typed nature of JavaScript, it is trivial to change the configuration.

**Why is HMR not preserving my local component state?**

HMR state preservation comes with a number of gotchas! It has been disabled by default in both `svelte-hmr` and `@sveltejs/vite-plugin-svelte` due to its often surprising behavior. You can read the details [here](https://github.com/sveltejs/svelte-hmr/tree/master/packages/svelte-hmr#preservation-of-local-state).

If you have state that's important to retain within a component, consider creating an external store which would not be replaced by HMR.

```js
// store.js
// An extremely simple external store
import { writable } from 'svelte/store'
export default writable(0)
```
