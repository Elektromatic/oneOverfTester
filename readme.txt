C----------------------------------------------------------------------------
C  			          oneOverfTester                  
C----------------------------------------------------------------------------
C
C  This pd patch creates "generative music" in conjunction with a Elektron 
C  Digitone synthesizer.
C
C  This patch generates 1/f noise based on the technique described in "White,
C  Brown, and Fractal Music" by Martin Gardner.
C  https://labs.la.utexas.edu/gilden/files/2016/04/Gardner-WhiteBrownFractalMusic.pdf
C
C  The 1/f noise is used to generate musical notes, accents for those notes, 
C  the length of the musical notes, and the duration of their portamento.
C
C  It also uses a "quantizer" modeled after Harmonaig Instruo eurorack module. 
C  https://www.modulargrid.net/e/instruo-harmonaig
C  The Instruo module is a chord generating quantizer and is used here to create 
C  a "pad".
C
C
C  Please see https://youtu.be/xJxycwq5i_k for an example of it's use.
C
C----------------------------------------------------------------------------
C  Requirements:   Pure Data <https://puredata.info/downloads/pure-data>
C----------------------------------------------------------------------------
C
Usage:  The file oneOverfTester.pd is the parent patch which contains the 
        rest of the modules.

              Explaination of the primary patches:

midiClockOut:  Generates the midi clock pulses sent to the Digitone.
expDist:       Sends random "bangs" that follow a Poisson distribution.
voss3Dice:     Uses the 3 dice method by Richard Voss to create 1/f noise.
eSeq:          Creates Euclidian rhythms.              
quantizer:     This patch models the Instruo by creating four note chords with various
               quality, voicing, and inversions.

Contributing: Any contributions to this project are welcome.

Acknowledgements: I'd like to thank Acreil for sharing his Pure Data patches. Namely; 
                  pois, rseq, and euclid, to create Euclidian rhythm patches used here.
