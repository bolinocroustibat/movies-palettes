# Movies Color Palettes

Generate color palettes from movie files (`.avi`, `.mkv` and `.mp4`).

The notebook runs in Google Colab. It mounts Google Drive and reads videos from `MyDrive/MOVIES`.

## Saving palettes

By default, each new palette is sent to the [cinematheque API](https://cinematheque.adriencarpentier.com/api/docs). That write needs a secret named `API_WRITE_KEY`. In Colab, open the key icon in the left sidebar, add the secret, and turn on notebook access for it.

In API mode, the notebook opens each file at the `path` returned for that movie (for example `MOVIES/Akira (1988)/file.mkv`, relative to `MyDrive` on the mounted Drive). File names on disk can stay messy as long as the path in the API is correct.

If you do not have an API key, set `BACKEND = "json"` in the notebook. It scans `MOVIES_DIR` on Drive and saves palettes to `palettes.json` there.

## Related Projects

This repository works in conjunction with [movies-palettes-frontend](https://github.com/bolinocroustibat/movies-palettes-frontend), which provides a web interface to display the generated color palettes.
