FFMPEG 
=====================
Use FFMPEG from PHP

Okay so this is really just a beginning.

Examples
---------------------

**Verify if this is a valid file**

> $ffmpeg = new FFMPEG('/path/to/your/video.mp4'); 

> var_export($ffmpeg->isValid()); //true; 

> var_export($ffmpeg->isVideo()); //true; 

> var_export($ffmpeg->isAudio()); //false; 


**Get metadata**

> $ffmpeg = new FFMPEG('/path/to/your/video.mp4'); 

> $metadata = $ffmpeg->getMetadata();

> var_export($metadata['duration']); // 30 seconds

> var_export($metadata['width']); // 1920

> var_export($metadata['height']); // 1080


**Convert video to flv**

> $ffmpeg = new FFMPEG('/path/to/your/video.mp4'); 

> $ffmpeg->convert('/path/for/the/new/flv/video.flv');
