# Astro Starter Kit: Blog with Strict TypeScript Configuration

The default Astro Blog sample does not include the `strict` TypeScript
configuration. When it is added, the existing sample will fail several
TypeScript validations.

This version adds additional settings and modifications to ensure TypeScript
works properly with a `strict` configuration.

## Visual Studio Code Issues

There are some issues with Code working properly with the `tsconfig.json` file
and consistently starting the TypeScript server to handle validating `.astro`
files.

The `ts-start.ts` file has been added for this purpose. Opening this file wakes
up the TypeScript server and forces it to really start checking for issues.

If you open a `.astro` file without having previously opened this file, any
issues may not be detected in the `.astro` file. In this case, you can force
the `.astro` file to be revalidated by doing the following:

-  Open the `ts-start.ts` file and leave it focused.
-  Use the Command Palette and run the "TypeScript: Restart TS Server" command.
-  Alternatively, just save the `ts-start.ts` file without any changes to force
   the TypeScript server to revalidate `.astro` files.
