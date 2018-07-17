
**July 16, 2018**

##### fl8 is the latest version of code that should be run...

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




##### Going forward I no longer need to support AppFrame

As I continue to upgrade this code over time **fl8** and forward
will go back to my own custom simple AppFrame / Drawer6 which
will be called Drawer6.

I will no longer need to port AppFrame over, remove the un-used code
etc...  But I will need to continue to port up AppDrawer and AppDrawerNavItem.

Leave the notes below here for historical purposes.

### Appframe

As of **fl7** the AppFrame and Drawer code are in the same directory.
In the past we had fl6 and fl6-appframe.  Now they are together.
In fl7 I remove all of the styling associated with the code
released

[mui appframe](https://github.com/mui-org/material-ui/commits/master/docs/src/modules/components/AppFrame.js)

and instead use the simple styling from Drawer6.  By doing this Drawer6
and AppFrame are essentially the same code.  In the future it would
be interesting to detail what the AppFrame styling brings to the table,
but for now Drawer6 is a proxy AppFrame as well as you can see from
the fact that the output / visualization is the same.
