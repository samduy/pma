### Lab 7-1

1. The program creates a service named `"Malservice"` to ensure that it continues running (achieve its persistence) when the computer restarted.
1. It uses a mutex (named `"HGL345"`) to make sure it will not create dupplicated service when it's already there.
1. Good host-based signatures: 
    * Mutex name: `"HGL345"`
    * Service name: `"Malservice"`
1. Good network based signatures:
    * Openned URL: `"http://www.malwareanalysisbook.com"`
1. Purpose of this program: It creates a service (for persistence), this service will create a thread and that thread will open Internet Explorer (IE) 8.0 and load a website at: `"http://www.malwareanalysisbook.com"`
1. The program sleep `-1` (`0xFFFFFFFFh`) seconds after creating the thread. It means, it will never finish its executing.
