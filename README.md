develop_breakage_on_windows
===========================

Simple setup for breakage of setup develop with binary files specified as script on windows

Intent
======

This python package demonstrates a failure of the develop command on windows when scripts are inary files.

The binary program included here is a simple hello world output to stdout.

When the develop command copies the scripts specified files, they are copied with the bare open() command that translates line endings on windows. This clobbers the destination.

Proof
=====

Run the following commands at the root of this sample:

    python setup.py develop
    python -c "from develop_break import module; module.main()"

Notice the crash. 
