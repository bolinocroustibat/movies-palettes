# Movies Color Palettes

Generate color palettes from movie files (`.avi`, `.mkv` and `.mp4`).

The notebook runs in Google Colab. It mounts Google Drive and reads the videos from `MyDrive/MOVIES`.

## Saving palettes

By default, each new palette is sent to the [cinematheque API](https://cinematheque.adriencarpentier.com/api/docs). That write needs a secret named `API_WRITE_KEY`. In Colab, open the key icon in the left sidebar, add the secret, and turn on notebook access for it.

Name each video file after the movie title. `Dick Tracy (1990).mkv` matches the title Dick Tracy.

If you do not have an API key, set `BACKEND = "json"` in the notebook. Palettes are saved to `palettes.json` in the same Drive folder, and nothing is sent to the API.

## Related Projects

This repository works in conjunction with [movies-palettes-frontend](https://github.com/bolinocroustibat/movies-palettes-frontend), which provides a web interface to display the generated color palettes.
