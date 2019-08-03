# pdfsandwich-without-unpaper

Pdfsandwich is a wrapper that embeds OCR-fonts in scanned PDFs. It uses (currently version 0.1.7) unpaper, which deskews and trims the scanned pages. Unfortunately, unpaper appears to be discontinued, [the last update was 2015](https://packages.qa.debian.org/u/unpaper.html)
. It also occasionally cuts off parts of the text. Luckily, there is an alternative: [scantailor](https://scantailor.org/). 

The shell script in this repo circumvents unpaper, using `pdfimages`, `scantailor` and `imagemagick` to prepare a PDF that is then OCRed by pdfsandwich. It just takes the filename as only argument, like so:

 `./ocrthispdf testpage.pdf`
