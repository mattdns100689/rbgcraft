# rbgcraft

## Fishing

### Overview

Automatic fishing in WoW, using a combination of: mouse/keyboard automation, audio processing, and basic computer 
vision techniques. See [YouTube Video](https://www.youtube.com/watch?v=5yYr2v4B-wY). 

This project was done for educational purposes.

![Alt text](images/status_blurred.png?raw=true)
![Alt text](images/status.png?raw=true) 
 

### Running the project

Setup the game as follows:
* Use default UI scale
* Turn off all nameplates
* Options -> Enable Sound -> Effects on 100% (all other sub volumes on 0%)
* Keybind fish action to 9, or change ```KEY_LOOKUP``` in the [config](fishing/config.py).
* Set up screen size, or change ```PIX_X``` and ```PIX_Y```, in the [config](fishing/config.py). Defaults to 2560 x 1080.
* Ensure "Click to Move" is turned off.

Install via
```commandline
python setup.py install
```

Run via:
```commandline
python -c "import fishing; fishing.fish()"
```
or
```python
import fishing
fishing.fish()
```
Then click on the game window to begin.

### Dependencies
* [Open CV](https://pypi.org/project/opencv-python/)
* [SoundCard](https://pypi.org/project/SoundCard/)
* [PyAutoGUI](https://pypi.org/project/PyAutoGUI/)

### Task List

- [ ] Audio signal inference to use only game sound, currently it listens to all desktop sounds.
- [ ] Work in background, so that user can run other applications actively.
- [ ] AFK and logout/login features.