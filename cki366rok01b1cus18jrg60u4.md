## Why sharing files/folders across devices is still messy in 2020?

This is going to be my long rant on the problems I faced when I wanted to transfer a large number of files between two devices and how I ended up exploring WebRTC.

So, recently I bought a new phone and I wanted to transfer all the files and folders (around 40GB) from my old phone to my windows laptop. Anyone would immediately think of connecting a USB cable and copying files. But my old phone has USB port issues, leaving me with the only wireless transfer. Well, with all the advancements in wireless technology it should be straightforward right? I am not sure if I did it right, at least my experience was horrible.

I started searching for different options I have available to transfer wirelessly. These are what I came up with:

- **Cloud Drives**: But it doesn't make sense for me to buy a subscription just for transferring 40GB of data. I want a way to transfer not to backup. So I discarded this option.
- **Wi-Fi Direct:** I installed  [Superbeam ](https://superbe.am/) - a popular Wi-Fi Direct app, and tried to transfer from my phone to my laptop. But transfer rates are very slow and connection keeps breaking, I have to start from the beginning every time. After many failed retries and after trying out other Wi-Fi Direct apps with the same problems, I gave up.
- **FTP**: I got fed up with all these apps and relied back on the standard FTP. Started an FTP server on my phone using  [Solid File Explorer](https://play.google.com/store/apps/details?id=pl.solidexplorer2)  and downloaded the files from my laptop. Even with this, transfer rates are slow but better than Wi-Fi Direct. And I faced similar connection drop issues. After a few tries somehow managed to transfer all the files.

After all this struggle, I started researching more to see if this is a real issue faced by everyone or just me. And I was surprised by the number of results I found on Hackernews and Reddit. I found many queries where people kept asking "What are the best ways to transfer files from android or ios to windows or mac etc.?" There are different apps available to do this job on different platforms but I failed to find a universal solution.  [Syncthing](https://syncthing.net/)  is the best solution that comes very close to my requirements. Haven't tested the transfer rates but I presume it should be equivalent to network bandwidth.

But I was not able to digest the fact that even in 2020 where all devices are wireless, I still need to install app or software on different devices to transfer files between them. Isn't transferring files or documents across devices is the primary reason why LAN/Internet is invented? Why do I need to fiddle with different software to achieve that? And, any non-technical person wouldn't be interested in installing software and setting them up, they will just go grab the USB cables and transfer.

Disappointed me started listing down the requirements of an ideal file/data transfer app, and it goes like this:

1. Ubiquitous and available on all platforms.
2. Requires minimal or no setup/installation. If I want to transfer a file to a friend who doesn't have it set up, we shouldn't be wasting more time in setting up than transferring the actual file.
3. Use the internet only when needed, if transferring between devices on the same network, my transfer speeds shouldn't be dependent on my internet bandwidth.
4. Be fast, like really fast, utilize the entire bandwidth.
5. Able to transfer any file, directory, or just a simple text message (like clipboard data).
6. Option to pause or resume when transferring large files, Handle connection issues reliably, and auto-retry on network failure without human intervention.
7. Transfer via a secure channel. At least it shouldn't be like anyone can easily sniff the data that is being transferred.
8. Simple and intuitive. No bloat. No account setup. Any layman should be able to use the app without any trouble.
9. And last but not the least, it should be free and open-source, which means no intermediate servers, preferably peer to peer.
10. Bonus: Transfer to multiple devices at once. An option to broadcast to all devices in the network.

After noting down the requirements, especially the first two points, I quickly realized, this is possible if it is a web app right? Browsers are available on every device, and web apps do not require any setup. And I am not the only one who realized this, many developers have already tried to solve this through a web app ([Snapdrop](https://snapdrop.net/),  [ShareDrop](https://www.sharedrop.io/)), but they don't meet other requirements quite well, specifically directory sharing and pause/resume option which are deal-breakers when transferring large files.

I started exploring how these existing apps work in the hope to extend them. The underlying technology that makes it possible to transfer files via browsers is  [WebRTC](https://webrtc.org/). It is a p2p protocol and an API that is available in all modern browsers. With my current understanding and research, I believe one can build a web app that satisfies the above-mentioned requirements using WebRTC. Transfer rates might not be super fast but we can achieve decent rates. I began to learn how WebRTC works and working on how feasible it is to build this app. Will keep posting my updates and progress in this blog.

Do let me know in the comments if there is an existing app that satisfies the requirements mentioned so that I am not reinventing the wheel. Also, let me know your opinion on having WebRTC as a base technology, Do you think we can solve this never-ending problem of wireless file transfer with WebRTC? If not which technology/protocol do you think fits this problem well?