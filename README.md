# YouTube Downloader Documentation

This documentation provides information on how to use the YouTube Downloader application, which allows you to download YouTube videos and playlists as audio files. The application is built using Node.js and utilizes the `yt-dl-playlist`, `youtubei`, and `ffmpeg` libraries.

## Installation

To install the YouTube Downloader application, follow these steps:

1. Install Node.js on your machine. You can download it from the official Node.js website: [https://nodejs.org](https://nodejs.org)

2. Install FFmpeg on your machine. FFmpeg is a multimedia framework that is required for audio conversion. You can download it from the official FFmpeg website: [https://ffmpeg.org](https://ffmpeg.org)

3. Open a terminal or command prompt and navigate to the directory where you want to install the application.

4. Run the following command to clone the repository:

   ```bash
   git clone <repository_url>
   ```

   Replace `<repository_url>` with the URL of the repository where the YouTube Downloader application is hosted.

5. Navigate to the cloned repository:

   ```bash
   cd <repository_directory>
   ```

   Replace `<repository_directory>` with the directory name of the cloned repository.

6. Install the application dependencies by running the following command:

   ```bash
   npm install
   ```

   This command will install all the required Node.js packages specified in the `package.json` file.

7. Once the installation is complete, you can start using the YouTube Downloader application.

## Usage

To use the YouTube Downloader application, follow these steps:

1. Open a terminal or command prompt and navigate to the directory where the application is installed.

2. Run the following command to start the application:

   ```bash
   node <application_file> [options] <id>
   ```

   Replace `<application_file>` with the name of the file containing the YouTube Downloader code.

3. Replace `<id>` with the YouTube video or playlist ID that you want to download.

4. Optional: You can use the following options with the application:

   - `-d, --debug`: Enable extra debugging output.
   - `-i, --info`: Show only the information about the video or playlist ID.
   - `-p, --playlist`: The ID provided is a playlist ID.
   - `-F, --ffmpeg [path]`: Path to the FFmpeg executable if it is not in the system's PATH.

5. Wait for the application to download the YouTube video or playlist. The downloaded audio file(s) will be saved in the current working directory.

## Example

Here's an example of how to use the YouTube Downloader application:

```bash
node youtube-downloader.js -p -i PL9KoUFcR9yXzYz2kih_4sxMkXlUWexLtn
```

This command downloads the audio from the YouTube playlist with the ID `PL9KoUFcR9yXzYz2kih_4sxMkXlUWexLtn` and displays information about the playlist.

## Events

The YouTube Downloader application emits the following events when downloading videos or playlists:

- `video-info`: Fired when video information is retrieved.
- `video-setting`: Fired when video settings are retrieved.
- `start`: Fired when the download of a video or playlist starts.
- `progress`: Fired periodically to indicate the conversion progress of a video.
- `complete`: Fired when the download of a video or playlist is completed.
- `error`: Fired when an error occurs during the download or conversion process.

You can listen to these events by registering event listeners on the `downloader` object.

