# src/hooks/

## Overview

Since many custom hooks are contained within a single file, they are not required to be in their own folder.

However, hooks can be grouped with other like hooks (a `useSession` and `useAuth` hook may both be nested under an `Auth/` folder)

The hooks `useProfile`, `useAuth` and `useTheme` may have a folder structure that looks like the following.

```
Good ✅

hooks/
- Auth/
-- index.ts
-- useAuth.ts
-- useSession.ts
- Profile/
-- index.ts
-- useProfile.ts
- Theme/
-- index.ts
-- useTheme.ts
```

Using this pattern, the `index.ts` file within each group folder would contain named exports for each hook.

```typescript
// hooks/Auth/index.ts

// import the auth servics
import { useAuth } from './useAuth.ts'
import { useSession } from './useSession.ts'

// export under Auth
export const Auth = {
  useAuth,
  useSession,
}
```

The following is also acceptable, and is preferred if there are no hooks that need to be grouped.

```
Also good ✅

hooks/
- useAuth.ts
- useSession.ts
- useProfile.ts
- useTheme.ts
- index.ts
```
