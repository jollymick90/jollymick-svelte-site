
# workspace
```
npx create-nx-workspace jollymick-svelte-site
```

# Svelte - NX
Plugin
```
npm install @nxext/svelte --save
```
Generate app
```
npx nx generate @nxext/svelte:application jm-site
```

Update file nx.json

```
"defaultProject": "jm-site"
```

Check
```
npm start
```

# Tailwind

Tailwind
```
npm install -D tailwindcss@latest postcss@latest autoprefixer@latest
```
Tools
```
npm install -D postcss-import@latest postcss-preset-env@latest node-sass@latest
```

### tailwind config
at root NX workspace create tailwind.config.js
```
'use strict';

module.exports = {
  mode: 'jit',
  purge: {
    content: [
      './apps/**/*.{html,svelte,tsx,ts,jsx,js,pcss,scss,css}',
      './libs/**/*.{html,svelte,tsx,ts,jsx,js,pcss,scss,css}',
    ],
    // PurgeCSS options
    // Reference: https://purgecss.com/
    //enable: production, // disable purge in dev
    options: {
      rejected: true,
      printRejected: true,
      safelist: ['html', 'body', 'dark'],
      safelistPatterns: [/svelte-/],
    },
  },
  /**
   * Enable dark mode
   */
  darkMode: 'class',
  theme: {
    extend: {},
  },
  variants: {
    extend: {},
  },
  plugins: [],
};

```
### postcss config 
at root NX workspace create postcss.config.js
```
module.exports = {
  plugins: {
    'postcss-import': {},
    // Reference: https://tailwindcss.com/docs/using-with-preprocessors
    'tailwindcss/nesting': {},
    tailwindcss: {},
    // Reference: https://github.com/csstools/postcss-preset-env
    'postcss-preset-env': {
      autoprefixer: {},
      stage: 3,
      features: {
        'custom-properties': false,
        // Reference: https://tailwindcss.com/docs/using-with-preprocessors
        'nesting-rules': false,
      },
    },
  },
};
```

loading config

open svelte.config.cjs and
```

```