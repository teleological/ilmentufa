ilmentufa
=========

'la ilmentufa' is a syntactical and not yet semantical parser for the Lojban language.

Read more about it at http://mw.lojban.org/index.php?title=La_Bangu:_ilmentufa


=== Requirements ===

For generating a PEGJS grammar engine from its PEG grammar file, as well as for running the IRC bot interfaces, you need to have Node.js installed on your machine.

For generating PEGJS engine, you may need to get the Node.js module 'pegjs'.
For running the IRC bots, you may need to get the Node.js module 'irc'.

However, as the necessary node_modules are already included in this project, I think you'll probably not have to download any of the aforementioned modules. ;)


=== Building a PEGJS engine ===

After having entered the ilmentufa directory, run the following command:
$ node camxes-builder

(Or camxes-exp-builder in the case of the experimental version of the grammar.)

Then, edit the generated/updated parser engine, and changes the first line so that it looks as shown below:

var camxes = module.exports = (function(){

If you skip this last step, the grammar engine will not be useable by the HTML interface nor by the IRC bot interface.


