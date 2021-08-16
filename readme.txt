NAME

tradelog - analyzer of logs from stock exchange trading
USE

tradelog [-h | --help] [FILTER] [COMMAND] [LOG [LOG2 [...]]
ELECTIONS

The COMMAND can be one of:
list-tick - a list of occurring stock exchange symbols, so-called "ticks".
profit - statement of total profit from closed positions.
pos - list of values of currently held positions sorted in descending order by value.
last-price - list of the last known price for each ticker.
hist-ord - list of histogram of the number of transactions according to the ticker.
graph-pos - list of graph of values of held positions according to the ticker.
  The FILTER can be a combination of the following:
-a DATETIME - after: only records after this date are considered (without this date). 
  DATETIME is in the format YYYY-MM-DD HH: MM: SS.
-b DATETIME - before: only records BEFORE this date (without this date) are considered.
-t TICKER - only records corresponding to the given ticker are considered. 
  With multiple occurrences of the switch, the set of all listed ticker is taken.
-w WIDTH - sets the width of the graph listing, ie the length of the longest line to WIDTH. 
  Thus, WIDTH must be a positive integer. Multiple occurrences of the switch is a faulty start.
-h and --help print help with a brief description of each command and switch.
