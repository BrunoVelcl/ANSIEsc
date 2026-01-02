# ANSIEsc

### About

AnsiEsc is an abstract Java class that enables easy usage of ANSI escape codes in CLI Java programs. It is designed as a
single class for maximum portability, it can be just dropped into a project without leaving a big fingerprint.
Whether you want to just add some color to your console projects or create elaborate menus it should have you covered.

### Note 

Support for ANSI escape codes varies between different terminals, so keep in mind that some features won't be supported
by every terminal.

### Example code

Instead of writing a long-winded document here, the best way to get the idea of what you can do and how to do it just
dump the following code snippet into an empty main method.

```java
        System.out.println(ANSI.Color.basicString("This is an example of using a basic color method.", ANSI.BasicColor.BLUE));
        System.out.println(ANSI.Color.basicString("This is an example of using a basic color method.", ANSI.BasicColor.GREEN));
        System.out.println(ANSI.Color.basicString("This is an example of using a basic color method.", ANSI.BasicColor.YELLOW));
        System.out.println(ANSI.Color.basicString("This is an example of using a basic color method.", ANSI.BasicColor.MAGENTA));
        System.out.println(ANSI.Color.basicString("This is an example of using a basic color method.", ANSI.BasicColor.CYAN));
        System.out.println(ANSI.Color.basicString("This is an example of using a basic color method.", ANSI.BasicColor.RED));
        System.out.println(ANSI.Color.basicString("This is an example of using a basic color method.", ANSI.BasicColor.WHITE));
        System.out.println(ANSI.Color.basicString("This is an example of using a basic color method.", ANSI.BasicColor.BLACK));
        System.out.println();

        System.out.println(ANSI.Color.brightString("This is an example of using a bright color method.", ANSI.BasicColor.BLUE));
        System.out.println(ANSI.Color.brightString("This is an example of using a bright color method.", ANSI.BasicColor.GREEN));
        System.out.println(ANSI.Color.brightString("This is an example of using a bright color method.", ANSI.BasicColor.YELLOW));
        System.out.println(ANSI.Color.brightString("This is an example of using a bright color method.", ANSI.BasicColor.MAGENTA));
        System.out.println(ANSI.Color.brightString("This is an example of using a bright color method.", ANSI.BasicColor.CYAN));
        System.out.println(ANSI.Color.brightString("This is an example of using a bright color method.", ANSI.BasicColor.RED));
        System.out.println(ANSI.Color.brightString("This is an example of using a bright color method.", ANSI.BasicColor.WHITE));
        System.out.println(ANSI.Color.brightString("This is an example of using a bright color method.", ANSI.BasicColor.BLACK));
        System.out.println();

        System.out.println(ANSI.Color.colorString("This is an example of using any rgb value to color a string. The rgb value is chocolate color.", 210, 105, 30));
        System.out.println();

        ANSI.Color.enableString(ANSI.BasicColor.CYAN);
        System.out.print("With this method you ");
        System.out.print("set the terminals output color ");
        System.out.println("until it is changed...");
        ANSI.Color.enableColor(255,99,71);
        System.out.println("by another toggle method...");
        ANSI.Color.disableForeground();
        System.out.println("or returned to default by using a disable toggle.");
        System.out.println();

        ANSI.Color.enableString(ANSI.BasicColor.BLACK);
        ANSI.Color.enableBackground(ANSI.BasicColor.WHITE);
        System.out.println("All of the above also applies for methods that set background color.");
        ANSI.Color.disableBackground();
        System.out.println("To disable background color use the method above.");
        System.out.println(ANSI.Color.colorBackground("If you want to use background color as a marker for some text do it like this.", 224, 255, 255));
        System.out.println();

        ANSI.reset();
        System.out.println("The above method disables all ANSI codes, use it as a master reset");
        System.out.println();

        ANSI.Style.enableItalic();
        System.out.println("Use styling methods to give your text various styles");
        ANSI.Style.enableUnderline();
        System.out.println("Just beware that not all terminals support every option.");
        ANSI.reset();
        System.out.println(ANSI.Style.bold("All style methods have toggle and single string versions just like the color methods."));
        System.out.println(ANSI.Style.strikethrough("And you can toggle every individual style on or off or use the master reset. "));
```

You can also use the Cursor methods for cursor manipulation, on terminals that support most ANSI escape codes you have 
enough tools here to make a small game if you wanted.

