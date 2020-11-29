# src/services/

## Overview

Each service should get it's own folder. Inside this folder, functions should be kept as modular as possible. Service names should be left simple.

For example

```
Good ✅

services/
- Users/
-- index.ts
-- browse.ts
-- read.ts
-- add.ts
-- edit.ts
-- update.ts
-- del.ts
```

```
Bad ❌

services/
- Users/
-- index.ts
-- browseUsers.ts
-- readUser.ts
-- editUser.ts
-- addUser.ts
-- deleteUser.ts
```

The `./services/index.ts` file should contain named exports for each service

```typescript
// services/index.ts

// Import the services
import { browse } from './Users/browse'
import { read } from './Users/read'
import { edit } from './Users/edit'
import { add } from './Users/add'
import { del } from './Users/del'

// Export them as a part of the Users object
export const Users = {
  browse,
  read,
  edit,
  add,
  del,
}
```

### Extra

Services should prefer the `BREAD` pattern over `CRUD`

```
Browse

Read

Edit

Add

Delete
```
