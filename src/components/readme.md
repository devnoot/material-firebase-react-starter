# src/components/

## Overview

Each component should conform to the following structure. For example, if we create a component named `PrimaryButton`, the following files would need to be created.

```
Good ✅

components/
- PrimaryButton/
-- index.ts
-- button.tsx
-- button.css
-- button.test.js
```

In this example, the file `index.ts` should export a named component called `PriamryButton`.

If we decide that we are going to have more than one button component, such as a `SecondaryButton` we could restructure like this.

```
Also good ✅

components/
- Buttons/
-- Primary/
--- index.ts
--- button.tsx
--- button.css
--- button.test.js
-- Secondary/
--- index.ts
--- button.tsx
--- button.css
--- button.test.js
-- index.ts
```

In this example, the `index.ts` file at the root of the `Buttons/` folder should contained named exports for both `PrimaryButton` and `SecondaryButton`
