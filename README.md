To get up and running

```
cd fl8
yarn [or] npm install
npm start
```

**July 16, 2018**

**fl8** is the latest version of code that should be run...

fl8 matches up with
[v1.4.0](https://github.com/mui-org/material-ui/releases/tag/v1.4.0)

This code is finished for awhile, in the future as material-ui
evolves I will periodically update this code with the latest
versions of the essential files documented below.

As Material-UI continues to evolve I will leave the versions
in place in their respective directories along with the
associated Readme files.

### The Details

withRoot.js should be an exact copy of
[withRoot.js](https://github.com/mui-org/material-ui/blob/master/examples/create-react-app/src/withRoot.js)

helpers.js should be an exact copy of
[helpers.js](https://github.com/mui-org/material-ui/blob/master/docs/src/modules/utils/helpers.js)

When ever changes happen to these (2) files you need to update this code...

[AppDrawer.js](https://github.com/mui-org/material-ui/commits/master/docs/src/modules/components/AppDrawer.js)

[AppDrawerNavItem.js](https://github.com/mui-org/material-ui/commits/master/docs/src/modules/components/AppDrawerNavItem.js)

#### AppDrawer Changes to file from original

Remove
```
import Link from 'docs/src/modules/components/Link';
import Typography from '@material-ui/core/Typography';
```

From this
```
import AppDrawerNavItem from 'docs/src/modules/components/AppDrawerNavItem';
```
to this
```
import AppDrawerNavItem from './AppDrawerNavItem';
```

From this
```
import { pageToTitle } from 'docs/src/modules/utils/helpers';
```
to this
```
import { pageToTitle } from './../utils/helpers';
```

Remove this code completely from the AppDrawer

```
<div className={classes.toolbarIe11}>
  <div className={classes.toolbar}>
    <Link className={classes.title} href="/" onClick={onClose}>
      <Typography variant="title" color="inherit">
        Material-UI
      </Typography>
    </Link>
    {process.env.LIB_VERSION ? (
      <Link className={classes.anchor} href="/versions">
        <Typography variant="caption">{`v${process.env.LIB_VERSION}`}</Typography>
      </Link>
    ) : null}
  </div>
</div>
```

#### AppDrawerNavItem Changes to file from original

From this
```
import Link from 'docs/src/modules/components/Link';
```
to this
```
import { Link } from 'react-router-dom';
```

Add in the **to** property to this line of code
```
<Link variant="button" activeClassName={classes.active} to={href} href={href} {...props} />
```
