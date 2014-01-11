# Erlangized File Utilities

This project is the start of a set of Erlang distribution-
aware command line utilities. The idea is to be able to reference files
accessible on remote Erlang nodes using familiar looking commands like
`ls` or `cp`.

Remote files are specified as `Node:Path`. For example, `mynode@host:/tmp/myfile`.
Relative path names are supported.

Currently only one utility is implemented, `erlcp`. Use it like you would
`cp`, but keep in mind that it doesn't support any command line options. It
doesn't set the magic cookie, so you'll want to set it in your `$HOME/.erlang.cookie`
file. Here's an example:

    erlcp mynode@host:/tmp/randomstats.txt .
