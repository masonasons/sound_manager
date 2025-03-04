# destroy
Stops and removes one or more sounds.

1. `bool sound_manager::destroy(sound_item@ handle);`
2. `int sound_manager::destroy(sound_item@[] handles);`
3. `int destroy(string&in owner);`

## Arguments (1):
- `sound_item@ handle`: A handle to the sound you want to remove.

## Arguments (2):
- `sound_item@[] handles`: An array of handles to the sounds you want to remove.

## Arguments (3):
- `string&in owner`: The sound's owner to remove. This will remove all sounds under this owner.

## Returns:
1. `bool`: true on success, false on failure.
2. `int`: The number of sounds that have been removed.
3. `int`: The number of sounds that have been removed.
