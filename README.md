## ConsoleWrite Usage ##

### Including the ConsoleWriter ###

	include('ConsoleWriter.php');

#### Create Javascript Block ####

	ConsoleWriter::consoleBlock('open');
	// YOUR WRITES GO HERE
	ConsoleWriter::consoleBlock('close');

#### Grouping Your Javascript Writes ####

	ConsoleWriter::consoleGroup('open', string _groupname_, );
 	// YOUR GROUPED WRITES GO HERE
	ConsoleWriter::consoleGroup('close');

* Parameters
  * _type_ Type of grouping
   * **open** Create a grouping that has visible contents
   * **end** Close out a grouping
   * **collapsed** Create a grouping that is collapsed by default
  * _groupname_ The classification you want to give your grouping

#### Writing to the Console ####

	ConsoleWriter::consoleLine(string _value_[, [string _type_], [string _key_]]);
		_or_
	ConsoleWriter::consoleQuickLine(string _value_[, [string _type_], [string _key_]]);

* Parameters
 * _value_ Value desired to write to the console
 * _type_ Type of write
  * **log**  Pretty much the same as informational
  * **info** Normal
  * **warn** Yellow Yield Sign
  * **error** Red and Nasty
 * _key_ Key value