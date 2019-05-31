# glpr

`glpr` is a visual interface, in the terminal for printing files using `CUPS`.
As the name suggests, it uses the Berkeley style `lpr` printing command to send the print job.
The interface is handled by `dialog` so should work on most systems, and even over SSH.

## Usage

To open up the print dialog for a given file simply execute
```
glpr /path/to/file
```
in your favourite shell.
This will open up a dialog box with the default print options on your system.
By selecting the appropriate item, you can change the following:

* Printer
* Page size
* Print quality
* Duplex mode
* Page range
* Copies
* Pages per sheet

Note that these are the options that are avilable on my printer, and that I often wish to change.
The options are hard-coded into the script so if you want different options you will have to change the script.
However, once an option is selected, all of the possible values for the selected printer will be automatically detected.

Upon changing the printer, all of the other options will be set to the default for that printer.
Hence it is recommended to change the printer first.

Once you're happy with all of the options simply select the `Accept` option from the main menu.
You will then be presented with the command that will be executed and you can choose whether or not to proceed.

## Limitations

* Printer options are hard coded into the script.
This list could be created autoamtically but I wanted a more concise interface so decided against it.
* Files can only be printed by specifying a filepath, whereas `lpr` accepts content from `stdin`.
This would be a good thing to implement next.
* This has only been tested on one printer from one computer in one network.

## References
* [Command-Line Printing and Options](https://www.cups.org/doc/options.html) on `cups.org`
