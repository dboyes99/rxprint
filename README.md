# rxprint
This package prints REXX source files with listing controls contained in REXX comments. The valid listing controls are:

/* RXPRINT:Title: <title> */ -  Sets the title string for listing. This 
                                line is printed at the top of each page
                                in bold letters. A blank line is inserted
                                following the title.

/*RXPRIMNT:Eject */ -           Generate an immediate skip to channel 1 
                                (new page)

/*RXPRINT:Bold */   -           Highlight following lines until a 
                                /* RXPRINT:Normal */ card is encountered.

/* RXPRINT:Normal */ -          Cancels the effect of a /* RXPRINT:Bold */
                                listing control

/* RXPRINT:Skip nn */ -         Insert nn blank lines at this location

/* RXPRINT:PageLen nn*/ -       Sets page length to nn lines. A new title
                                line is generated at the top of every page.

/* RXPRINT:Line nn */ -         Set line lenght to nn. The default is 132
                                chars.

Printer controls are implemented with standard ASA/machine-specific listing 
directives included in col 1 of the file. All output is shifted one column to the right to permit inserting the appropriate control characters.

This utility produces a LISTING file as output and can be printed using the 
PRINT fn ft fm ( CC command.







