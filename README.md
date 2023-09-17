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

```jsx
..foo
#or

input..foo
```
