# pgn-ocr
Bash script with a custom tesseract model to OCR algebraic chess notation from chess PDF books into PGN.
Most of these books use chess symbols that can't be read by ordinary English OCR.

I set it to a keybind in my window manager to conveniently get PGN from chess PDFs into my clipboard which can be pasted into Lichess studies and analysis.

The script will probably only work under X11 on Linux/BSD, but the .traineddata file may still be useful on other platforms.

## dependencies
* ImageMagick 7
* scrot
* sed
* tee
* tesseract
* xclip

## usage
You will need both the pgn-ocr script and the Chess.traineddata file.

When you run the script, your mouse cursor will turn into a selection tool like when taking a screenshot.
Screenshot the chess notation to be OCR'd and the resulting PGN will be printed to stdout and copied to your clipboard.

The script assumes Chess.traineddata is in the same folder as pgn-ocr. If it isn't please adjust `tdata_location` in the script.
