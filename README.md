# florida-mui

So I got this working with the
[v1.2.1](https://github.com/mui-org/material-ui/releases/tag/v1.2.1)

### The Details

withRoot.js should be an exact copy of
[withRoot.js](https://github.com/mui-org/material-ui/blob/master/examples/create-react-app/src/withRoot.js)

helpers.js should be an exact copy of
[helpers.js](https://github.com/mui-org/material-ui/blob/master/docs/src/modules/utils/helpers.js)

When ever changes happen to these (2) files you need to update this code...

[AppDrawer.js](https://github.com/mui-org/material-ui/commits/master/docs/src/modules/components/AppDrawer.js)

[AppDrawerNavItem.js](https://github.com/mui-org/material-ui/commits/master/docs/src/modules/components/AppDrawerNavItem.js)

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
