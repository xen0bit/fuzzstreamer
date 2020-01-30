# fuzzstreamer
Python HTTP server that serves fuzzed HTML DOM with arbitrary sized bytes per chunk.

Transfer-Encoding: Chunked

Browsers eagerly try to auto-close HTML tags to be "first to paint" before page has finished loading. Chunked encoding causes eager parsing bugs in all browsers.

This tool aims to fuzz browser parsing via chunked encoding rather than loading generated HTML from disk.

DoS bugs can be found in Chrome/Firefox in a few minutes. Other bugs including spoofing attributes in the URL bar have also been found using this tool.
