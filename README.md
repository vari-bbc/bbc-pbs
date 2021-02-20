# bbc-pbs
scripts useful when using PBS job management system

# Usage

## pbstdout and pbstderr

`pbstdout` and `pbstderr` read the STDOUT and STDERR output, respectively, from a job managed by PBS. These scripts take as a single argument the jobid. For example:

`$ pbstdout 1269034`

## pbsfollow

`pbsfollow` reads the last lines of both the STDOUT and STDERR files for a job managed by PBS. When the script runs, the user is placed in a view that
updates every 5 seconds. So, new lines added to STDOUT and STDERR will be continuously displayed. Like `pbstdout` and `pbstderr` it takes as a single
argument the jobid. And, `pbsfollow` uses `pbstdout` and `pbstderr`, so these commands need to be in your default path.

## nodetop

`nodetop` displays a top window of processes running on a specific node in a cluster managed by PBS. It updates every 15 seconds. `nodetop` takes as a single argument the
name of the node. For example:

`nodetop node095`

