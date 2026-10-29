# DishPong

A Pong game played by a small simulated culture of spiking neurons, inspired by the "brain cells in a dish" experiments.

**Play it here:** https://deborabuilds.github.io/dishpong/

## How it works

- The ball's height is sent to the dish as spikes on 16 sensory electrodes.
- 16 motor neurons each vote for a paddle position.
- A miss floods the dish with random noise. A hit gives it a calm, predictable beat.
- Synapses keep short-lived eligibility traces. A hit strengthens the connections that were active. A miss weakens them and shakes them up, more strongly the more often the dish is failing.
- Calm leads to exploitation, noise leads to exploration. In simulation the hit rate rises from about 40% to about 80% within roughly 100 rallies.

This is a simplified model, not real neuron biology: hits and misses change the weights directly, like a reward and penalty rule.

## Credits

This is an independent implementation, written from scratch. The idea was inspired by the "DishBrain" experiment by Cortical Labs (Kagan et al., 2022), in which cultured neurons learned to play Pong, and by a video from Instagram account [@vibecodingiseasy](https://www.instagram.com/vibecodingiseasy/).

## Controls

- Speed buttons (1x to 256x) let you watch the dish learn faster.
- **Play myself**: move the paddle with the mouse, touch, or the Up/Down arrow keys (W/S also work).
- **New dish**: restart with fresh random connections.
- **Sound**: optional calm beat on a hit and a noise burst on a miss.

## Run it locally

It is a single file. Download `index.html` and open it in a browser. If your browser shows a blank page, serve the folder with `python3 -m http.server` and open http://localhost:8000.
