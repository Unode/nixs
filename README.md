# nixs

nixs for *nix search* is a quick command-line tool for searching nix/nixos packages using the same strategy and files as [the online package search](https://nixos.org/nixos/packages.html).

## Usage

Add nixs to your path and run:

    nixs <pattern>

such as:

    nixs disn

and you should see something like:

    Attribute name  Package name  Description
    disnix          disnix-0.6.1  A Nix-based distributed service deployment tool
    disnixos        disnixos-0.5  Provides complementary NixOS infrastructure deployment to Disnix

## Cache

### Force update

This script uses the package cache from the above URL.  
The cache is re-downloaded automatically if the file is older than 6 hours.

If for some reason you still need to force an update you can do so with:

    nixs -u <pattern>

### Ignore age

If on the other hand you don't want to automatically update every 6 hours or if you are working offline after having downloaded the cache you can use:

    nixs -i <pattern>

to ignore the age of the cache.
