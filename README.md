# Creativitease

## Installation

* Install node-red
* npm install node-red-contrib-osc
* install creativitease

### Supercollider

* scsynth and synthefs
* jackd for RPi

### Processing

* Install processing from https://processing.org/download/
* Start processing and goto Sketch > Import Library > Add Library ...
* Select oscP5 from the list and click on Install (then close tne contribution manager window)

## Start up

### Audio setup

* Instruments into mixer Line Ins
* Mixer Aux Send into Focusrite Guiter input (jack to jack)
* Focusrite phono pair via stereo jack into Mixer Aux Return
* Mixer Main out (R) to speaker
* Set Focusrite guitar input level so that there's no distortion
* Mixer Aux level to max (and Main Level adjusted up) on those you want to sample
* Mixer Level straight up for those you want to hear on the output

### Supercollider (do this first)

* If using ScarlettSolo make sure that both system input and and system output are using it or you might get a sample rate conflict
* Start supercollider and boot server
* If you get "input and output sample rates do not match. 48000 != 44100
could not initialize audio." try "s.options.sampleRate = 48000; 
s.reboot; "

### Node-red

* Start node-red
* Start point browser to http://127.0.0.1:1880
* Output is probably mono so make sure everything is plugged in to RH channel
*

### Debug

* s.dumpOSC(1);