# Simply Stream

> A video streaming application based on the FFmpeg library. It does not perform adaptive bitrate streaming.

### Workflow - 
> 1. The file is uploaded on the server using multer.
> 2. File uploaded should be short (recommended up to 75-80 MB and max 1080p)
> 3. The server uses the FFmpeg library to convert the provided video into HLS (HTTP live streaming format) format.
> 4. Then the video URL of that file is passed to the frontend client. The Frontend client makes use of the video.js library to play the video on the video player.
>

### Code implementation : 

#### 1. To run the server, in the root directory run the following command : 
      npm run start
#### 2. Then fire a new terminal move to the frontend directory and use the following command to run the application.
      cd frontend
      npm run dev

### Note - 
1. The video uploading takes time.
2. The video URL passed to the client is hard-coded. So to use the application, you have to replace the videoLink present in the App.jsx with your uploaded Video URL. 
   You can get that from the response that you receive from the server after uploading the video.
3. Also you can study how the server is sending segments to your browser through the browser's network tab.
4. The whole application is based only on the FFmpeg command.
