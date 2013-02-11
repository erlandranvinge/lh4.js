lh4.js
======
Javascript implementation of LHA extractor (-lh4-, static huffman) format. Requires ArrayBuffers (HTML5).

Usage
------

    var lha = new LhaReader(new LhaArrayReader(input));
    var output = lha.extract(Content.PakFileName, function(done, total) {
	    console.log('Extracting LHA data: ' + (done / total * 100) + '% complete.');
    });

All input/output is passed as an Uint8Array. In order to support new formats (e.g. reading data directly from an URL), implement your own versions of LhaArrayReader/LhaArrayWriter objects. 


