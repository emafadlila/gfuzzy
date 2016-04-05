# Dependencies #

The following packages need to be installed:
  * Python 2.6 (the code has been checked to work well with this version, there are no guarantees whatsoever with other version of Python).
  * Python bindings for the protocol buffers: http://code.google.com/p/protobuf/
  * Nose tests framework: http://somethingaboutorange.com/mrl/projects/nose/

# Check out the code #
We use subversion as our source control system. In order to get the latest version of the code, just type:

`svn checkout http://gfuzzy.googlecode.com/svn/trunk/ gfuzzy-read-only`
`cd gfuzzy-read-only`
# Compile the protocol buffer interface #
The protocol buffer specification file has to be compiled to a python script. You MUST run the following command:

`make`
# Run the tests #
In order to make sure that the code distribution works well and that you have the required modules, run the tests as follow:

`make test`
# Tutorial #

Once all tests pass, you can go to the [Tutorial](Tutorial.md) page, which will show you some of the gfuzzy basics.