# update_sound
Updates a sound.

`bool sound_manager::update_sound(sound_item@ handle, vector position, bool force = false);`

## Arguments:
- `sound_item@ handle`: A handle to the sound you want to update.
- `vector position`: The sound's position in vector form to update.
- `bool force = false`: Should the sound update by force? See remarks.

## Return value:
`bool`: true on success, false on failure.

## Remarks:
The soundd will always update if one of the following things happens regardless of the `force` parameter:
- If the sound's position, listener, or rotation is different.
