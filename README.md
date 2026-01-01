This is the first few lines from the script.  Executing this command from within
bash will add a time-stamped, 1 line string of text into the designated file.

It can be used to record anything you want, from doing the laundry, to selling the farm, etc.


# Name: didlog
#
# Purpose: Record a one-line description of what has been done into a log file
#
# Arguments: event to be recorded, optional time, optional date
#
# Author: Ed Drouillard on March 19, 1994
#
##########################################################################
#
# Arguments:
#	if none specified, shows recent entries in the file
#   if only "-e" is specified, edits the log file using $EDITOR if set, vi otherwise
#   if only "-l" is specified, shows the name of the log file
# 
# Variables:
#
# event: event, which must be in quotes, to be recorded in the file
# time: time to be recorded in the file, in the form HH:MM
#	current time is used if not specified
# date: date to be recorded in the file, in the form YY/MM/DD
#	current date is used if not specified
#	if "y" is specified, then yesterday's date is used
#
# set -xv

DIDLOGFILE=.perslog # the default name of the logfile which will have the year appended
