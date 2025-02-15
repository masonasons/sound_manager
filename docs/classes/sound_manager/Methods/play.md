# play
Play a sound.

1. `stationary_sound@ sound_manager::play(string filename, bool looping = false, bool persist = false, bool wait = false, bool immediate = true, float pan = 0, double pitch = 100, float volume = 0, string[]@ fx = null, string owner = "");`
2. `positional_sound@ sound_manager::play(string filename, vector v, float rotation = 0.0, bool looping = false, bool persist = false, bool wait = false, bool immediate = true, float pan = 0, double pitch = 100, float volume = 0, string[]@ fx = null, string owner = "", int leftrange = 0, int rightrange = 0, int backwardrange = 0, int forwardrange = 0, int lowerrange = 0, int upperrange = 0);`

## Arguments (1):
- `string filename`: The sound to play.
- `bool looping = false`: Toggle sound looping.
- `bool persist = false`: Should the sound be cleaned up when it is finished playing?
- `bool wait = false`: Should the program be paused while the sound is playing?
- `bool immediate = true`: Should the sound play immediately the moment this sound is initialized?
- `float pan = 0`: The pan of the sound.
- `double pitch = 100`: The pitch of the sound.
- `float volume = 0`: The volume of the sound.
- `string[]@ fx = null`: effects to set.
- `string owner = ""`: The owner of the sound. Usually empty.

## Arguments (2):
- `vector v`: The sound coordinate in vector form.
- `double rotation = 0.0`: The rotation of the listener.
- `int leftrange,  rightrange,  backwardrange,  forwardrange,  lowerrange,  upperrange`: The sound range. They are set to 0 by default.

## Return value:
`sound_item@`: The sound item class (e.g. positional or stationary) on success, null otherwise.

## Remarks:
To determine which sound class it is, you can use casting or specify the return value, for instance, `positional_sound@ s = sound_manager.play`. You can also use the `type` property to verify the sound type. For a list of available sound item types, see `sound_item_types` enum.
