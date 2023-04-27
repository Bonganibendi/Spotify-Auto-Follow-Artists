# Spotify Auto-Follow Artists

This Python script allows you to automatically follow all artists from your saved albums on Spotify. The script uses the Spotipy library to interact with the Spotify Web API and requires OAuth 2.0 authentication to access your Spotify account.

## Dependencies

- Spotipy: `pip install spotipy`

## Usage

1. Create a new app on the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/applications) to get your `client_id`, `client_secret`, and set a `redirect_uri`.
2. Replace the placeholders in the script with your actual `client_id`, `client_secret`, and `redirect_uri`:

   ```python
   client_id = "Enter Your Client ID Here"
   client_secret = "Create Client Secret"
   redirect_uri = "Create a Redirect URI"
   ```

3. Run the script:

   ```
   python auto_follow_artists.py
   ```

   The script will prompt you to log in to your Spotify account and grant the necessary permissions.

4. After successfully authenticating, the script will automatically follow all artists from your saved albums and print a confirmation message:

   ```
   Successfully followed all artists from saved albums.
   ```

## Functions

- `get_saved_albums_artists(sp)`: Retrieves the artist IDs from your saved albums.
- `follow_artists(sp, artists)`: Follows the specified artists on Spotify.

Please note that this script only supports following artists from saved albums and does not handle playlists or individual tracks.
