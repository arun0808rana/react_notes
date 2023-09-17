# Development Notes

### Absolute Path Instructions

- Modify your `vite-config.js` file with aliases.

  
#### `vite-config.js`
```javascript
import { defineConfig } from "vite";
import react from "@vitejs/plugin-react";

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [react()],
  resolve: {
    alias: [
      { find: "@assets", replacement: "/src/assets" },
      { find: "@components", replacement: "/src/components" },
      { find: "@hooks", replacement: "/src/hooks" },
    ],
  },
});
```

### Emmet for className={styles.foo} instead of className="foo"

#### Pre-requisite

..foo expands to styleNam={styles.foo}. To make it className={styles.foo} you have to add the following config to settings.json at root level of your json. To open settings.json, press ctrl+, or you can navigate File > Preferences > Settings in vscode. There at top right corner there is an icon to open settings.json file.

```javascript
"emmet.syntaxProfiles": {
    "jsx": {
        "markup.attributes": {
            "class*": "className",
        },
        "markup.valuePrefix": {
            "class*": "styles"
        }
    }
}
```


```jsx
..foo
#or

input..foo
```

Source: https://code.visualstudio.com/updates/v1_80#_improved-emmet-support-for-css-modules-in-jsxtsx
