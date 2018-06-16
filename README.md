# florida-mui

So I got this working with the
[v1.2.0](https://github.com/mui-org/material-ui/releases/tag/v1.2.0)

[here is the commit time stamp](https://github.com/mui-org/material-ui/commit/4ff3588dd268a83704cc55bfdbddb935c2f130ec)

This translates to **June 8, 2018**

I ported this over from
[this working version](https://github.com/stormasm/react-router-mui)
I had gotten working while I was in Florida...

### The Details

withRoot.js should be an exact copy of
[withRoot.js](https://github.com/mui-org/material-ui/blob/master/examples/create-react-app/src/withRoot.js)

helpers.js should be an exact copy of
[helpers.js](https://github.com/mui-org/material-ui/blob/master/docs/src/modules/utils/helpers.js)

When ever changes happen to these (2) files you need to update this code...

[AppDrawer.js](https://github.com/mui-org/material-ui/commits/master/docs/src/modules/components/AppDrawer.js)

[AppDrawerNavItem.js](https://github.com/mui-org/material-ui/commits/master/docs/src/modules/components/AppDrawerNavItem.js)

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
