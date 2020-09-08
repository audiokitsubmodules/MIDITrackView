# MIDI Track View

This is a demo of AKMIDITrackViewm, a class that contains the code for a horizontal MIDI sequencer view, similar to what you see
in most Digital Audio Workstations.
To add this view to your app, it's as simple as specifying the size/position of the view you
would like, giving it a MIDI File URL and track number, adding an AKMIDISampler,
adding an AKAppleSequencer,
 and adding the track view to the view controller

For example:

```
var trackView1: AKMIDITrackView = AKMIDITrackView(frame: CGRect(x: , y: , width: , height: ),
midiFile: AKMIDIFile(url: urltoyourmidifile),
trackNumber: The MIDI track number you want to display,
 sampler: AKMIDISampler,
 sequencer: AKAppleSequencer)

//Inside View Controller

self.view.addSubview(self.trackView1)

self.trackView1.play()
```
If you are using an AKAppleSampler or AKSampler, sequencer, etc,
you will want to play the track directly before you play through the sequencer
so the sound is synced with the playback.

AKMIDITrackView is still in development. I have tried loading some forms of MIDI files, and they do not yet work.
I have recently set up the playback to be synced with automated tempos which change over time.
