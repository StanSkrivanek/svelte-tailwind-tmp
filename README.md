# Svelte 5 & TailwindCSS Template

This is a template for a Svelte 5 project with TailwindCSS and Typescript. It is based on the official Svelte template.

## Installed packages

- TailwindCSS
- PostCSS
- Autoprefixer

## Fonts

fonts are in the `static/fonts/inter` folder. The fonts are:

- [Inter](https://fonts.google.com/specimen/Inter)

## CSS

Template have :
- applied **CSS Reset** based on the [Josh Comeau Modern CSS Reset](https://www.joshwcomeau.com/css/custom-css-reset/)
- basic custom color set

---

**NOTE:**  
Svelte inspector is not working in Svelte 5 for now. When will be available, it will be added to the template.

Optionally a CSP _(Content Security Policy)_ can be added to the `.svelte.config.js`.

[Article about CSP](https://dev.to/askrodney/sveltekit-content-security-policy-csp-for-xss-protection-589k)

```javascript
import adapter from '@sveltejs/adapter-auto';

/** @type {import('@sveltejs/kit').Config} */
const config = {
	kit: {
		adapter: adapter(),
		csp: {
			mode: 'hash',
			directives: {
				'script-src': ['self', 'unsafe-inline'],
			}
		}
	},
	vitePlugin: {
		inspector: {
			// change shortcut
			toggleKeyCombo: 'meta-shift',
			// hold and release key to toggle inspector mode
			holdMode: true,
			// show or hide the inspector option
			showToggleButton: 'always',
			// inspector position
			toggleButtonPos: 'bottom-right'
		}
	}
};

export default config;
```

