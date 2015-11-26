FFMPEG 
=====================
Use FFMPEG from PHP

Okay so this is really just a beginning.

Examples
---------------------

**Verify if this is a valid file**

> $ffmpeg = new FFMPEG('/path/to/your/video.mp4');

> if(!$ffmpeg){ print 'Fail FFMPEG'; }

> echo $ffmpeg->isValid(); //true; 

> echo $ffmpeg->isVideo(); //true; 

> echo $ffmpeg->isAudio(); //false; 


**Get metadata**

> $ffmpeg = new FFMPEG('/path/to/your/video.mp4');

> if(!$ffmpeg){ print 'Fail FFMPEG'; }

> $metadata = $ffmpeg->getMetadata();

> echo $metadata['duration']; // 30 seconds

> echo $metadata['width']; // 1920

> echo $metadata['height']; // 1080


**Convert video to flv**

> $ffmpeg = new FFMPEG('/path/to/your/video.mp4');

> if(!$ffmpeg){ print 'Fail FFMPEG'; }

> $ffmpeg->convert('/path/for/the/new/flv/video.flv');
