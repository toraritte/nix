# Quick Tour: Build a Simple Package

This       section      shows       how       to      package       [GNU
Hello](http://www.gnu.org/software/hello/hello.html)  (a   program  that
prints out the text “Hello, world\!”), test it, and add it to the [**Nix
Packages collection**](https://github.com/nixos/nixpkgs).

The general steps to achieve these goals:

1. *Write a **Nix derivation expression** for the package.*

   This  is  a  file  that  contains a  **function**  written  in  the  Nix
   expression language;  it describes all  the inputs involved  in building
   the package, such as dependencies, sources, and so on.

2. *Write a **builder**.*

   This  is a  script  that builds  the  package from  the  inputs, and  is
   referenced in the  package's Nix expression (step 1.).  Typically it's a
   shell script (e.g., `bash`), but it can be written in any language.

3. *Build and test your new package.*

   Build your new package using Nix's  command line  tools  to test if it's
   broken before installing it globally on your system.

4. *Add the package to the [**Nix Packages collection**](https://github.com/nixos/nixpkgs).*

   Update `pkgs/top-level/all-packages.nix`  with the call of  the function
   written in step 1.
