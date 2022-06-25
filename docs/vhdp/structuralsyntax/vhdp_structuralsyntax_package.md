---
id: package
title: Package
sidebar_label:  Package
---

## Definition

Can be added to [Main](/docs/vhdp/structuralsyntax/main) or [Component](/docs/vhdp/structuralsyntax/component) in the brackets. Package allows to use own datatypes and constants in the whole project.

## Example
```vhdp
Main
(
    Package <Package Name>
    (
        TYPE <Type Name> (a, b, c …);
    );
    LED : OUT STD_LOGIC := '0';
)
{
    ...
}
```

You can put Package in a separate file with braces and can declare functions and SeqFunctions next to types and constants.

## Example
```vhdp
Package <Package Name>
{
    TYPE <Type Name> (a, b, c …);

    Function <Function_Name> (return INTEGER; value_in : INTEGER)
    {
        ...
    }
}
```

By default every VHDP file uses all Packages. If you want to choose only some, you can use Include.

## Example
```vhdp
Main
(
    Include
    (
        <Package Name>.all,
        ...
    );
)
{
    ...
}
```

To use other IEEE libraries, add them to Include. By default "IEEE.STD_LOGIC_1164" and "IEEE.numeric_std" is included.

## Example
```vhdp
Main
(
    Include
    (
        IEEE.STD_LOGIC_1164.all,
        IEEE.std_logic_unsigned.all,
        ...
    );
)
{
    ...
}
```
