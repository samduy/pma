### Lab 7-1

1. The program creates a service named `"Malservice"` to ensure that it continues running (achieve its persistence) when the computer restarted.
1. It uses a mutex (named `"HGL345"`) to make sure it will not create dupplicated service when it's already there.
1. Good host-based signatures: 
    * Mutex name: `"HGL345"`
    * Service name: `"Malservice"`
1. Good network based signatures:
    * Openned URL: `"http://www.malwareanalysisbook.com"`
    * [FIX] User-agent: `"Internet Explorer 8.0"`
1. Purpose of this program: It creates a service (for persistence), this service will create a thread and that thread will open Internet Explorer (IE) 8.0 and load a website at: `"http://www.malwareanalysisbook.com"`
[FIX] The program actually:
      * Wait until 0:00 AM Jan 1st 2100 (`834h`)
      * Create 20 (`0x14h`) threads to run at the same time
      * Each thread will request to that website, loop (request again) and never finish.
      * The purpose is to establish a DDoS attack.
1. The program sleep `-1` (`0xFFFFFFFFh`) seconds after creating the thread. It means, it will never finish its executing.

### Lab 7-2

1. (no idea) [FIX] The program has no persistence.
1. Purpose of this program
      * Navigate to a website at: `http://www.malwareanalysisbook.com/ad.html`
      * GoSearch (twice) --> Navigate --> Refesh --> Refresh2
      * [FIX] The program displays and advertisement webpage to the user.
1. (no info) [FIX] The program finishes executing after displaying the advertisement.
