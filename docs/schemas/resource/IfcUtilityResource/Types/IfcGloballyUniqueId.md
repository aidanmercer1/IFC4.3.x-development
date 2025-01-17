# IfcGloballyUniqueId

An _IfcGloballyUniqueId_ holds an encoded string identifier that is used to uniquely identify an IFC object. An _IfcGloballyUniqueId_ is a Globally Unique Identifier (GUID) which is an auto-generated 128-bit number. Since this identifier is required for all IFC object instances, it is desirable to compress it to reduce overhead. The encoding of the base 64 character set is shown below:

> <font face="Courier New" size="-1">                   1         2         3         4         5         6

		<br> 0123456789012345678901234567890123456789012345678901234567890123<br>

		"0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz_$";

        </font>
>


The resulting string is a fixed 22 character length string to be exchanged within the IFC exchange file structure.

> NOTE  Refer to the BuildingSMART website ([www.buildingsmart-tech.org](http://www.buildingsmart-tech.org)) for more information and sample encoding algorithms.

> HISTORY  New type in IFC1.5.1.
