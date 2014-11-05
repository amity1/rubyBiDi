rubyBiDi
========

This package contains a function that converts your input logical UTF-8 string into a visual string according to the Bidi algorithm
found in http://www.unicode.org/reports/tr9/

Requirements:
* Ruby 1.9
* The Ruby llibrary 'weakref'

The conversion function is found in "bidi.rb"

To use the conversion function:
1. Define an object of class 'Bidi'. We'll call this object bidi.
2. call 'bidi.to_visual <your string> <default paragraph direction>'
   The values for default paragraph direction:
     * 'R' or 'RTL' - Right to Left text.
     * 'L' or 'LTR' - Left to right text.
     * other values or omitted - the default for each paragraph.

Constants:
* Bidi.RLE - Right to left embedding. 
* Bidi.LRE - Left to right embedding.
* Bidi.RLO - Right to left override.
* Bidi.LRO - Left to right override.
* Bidi.PDF - Pop Directional Formatting. 
* Bidi.RLM - Right to left mark.
* Bidi.LRM - Left to right mark.

To run a script that calls 'bidi.to_visual', type
ruby -Ku <script name.rb>

'K' stands for Kanji, letters commonly used in japan and in China. this will cause Ruby to interpret the extended character set as UTF-8 character set, and will prevent the embarrassing error message 'invalid multibyte char (US-ASCII)'.


"bidi.rb" also contains a method named "to_utf8_char", which extends the Integer class. You can use it to define additional UTF-8 characters.
