<header>
<h1> The Copying Technique </h1>
<aside> or: how to create the perfect sound </aside>
<p> _____________________ </p>
</header>

<p> In the past year and a half, I have been preoccupied with some concepts which I think may be of use to you. Rather than keeping them hidden, I felt the time is right to share them, so that they may help you better understand the world. </p>

<p> <b> I'm quite certain that anything can be copied, and made into sound, which would then have the effect of the thing it is representing. </b> </p>

<p> I'll admit I don't know if this technique is even hidden, since it is so obvious. But maybe sometimes it is necessary for someone to state the obvious, so that others may see it as well. </p>

<p> First, choose a file that represents your desired "effect". I find myself most gravitating towards interesting substances, but really, you can choose any effect. </p>

<p> Two key rules: You can't copy something that doesn't exist, and the more specific you are, the better. There are slight exceptions, and I welcome any attempts to prove me wrong.</p>

<p> For an example, I will use a file representing "blessed water", an invention by <a href="https://twitter.com/NgoloTesla">N'Golo Tesla</a>. See the example below: </p>

<img src="https://i.ibb.co/2332TGsZ/blessed-water.png" alt="blessed-water">

<p> We will plug the image, which is a good representation of our desired substance, into a sha256 hashing function. It's just a mathematical function that spits out a number, or a string of letters, depending on how you look at it. </p>

<p> A good site for it is <a href="https://emn178.github.io/online-tools/sha256_checksum.html">emn178</a>.</p>

<p> Plugging it into the hashing function, we get <em>84ae51b4dfb7728d1247158985264cef91ed875fb13407066084cb2fdc7157e9</em>. Doesn't matter, all you need to know is that this "number" is unique to this file, and thus is "linked" to it. </p>

<p> Now, let's do something interesting with that number. Really, you could do anything to make it work, but what I'll do is attempt to create the smallest unique sound the represents the "number", via this python script. </p>

<dl>
<code>
	<dt> import wave<br> </dt>
	<dt> with wave.open("your-file-name.wav", 'wb') as file: <br> </dt>
	<dd>file.setnchannels(1)<br></dd>
	<dd>	file.setsampwidth(2)<br> </dd>
	<dd>	file.setframerate(44100)<br> </dd>
	<dd>	a = bytes(b"put hash here") <br> </dd>
	<dd>		file.writeframes(a) <br> </dd>
</code>
</dl>

<p> <i>change your-file-name.wav and put-hash-here to your desired filename and hash</i></p>

<p> This code is nothing special. It will just generate a file with the hash result as its "audio". It's going to be hard to listen to it, but you should feel a small effect of the substance/effect you desired.</p>

<p> One thing you will notice is that the file is very short. This is by design. Since the file is short, the effect is stronger when the file is repeated. </p>

<p> To make it longer, download Audacity, import the file, select Effect-&gt;Special-&gt;Repeat-&gt;and repeat for maybe 10,000 times. Audacity will tell you that it will take 3 hours or something, but it has never taken me longer than 2 minutes.</p>

<p> And that's it. You got your file! Now you can play it. I'm not affiliated with <a href="https://infopathy.com/">Infopathy</a>, but their devices are good because they encompass all the frequency range and do minimal digital signal processing, which can alter the signal. </p>

<p> For the strongest effect, you would then play it to water that you shook. If you don't have money or time, you could shake a water bottle vigoursly for 10 seconds, then put overear headphones on it, and let it play for 20 minutes, maybe less.</p> 

<p> That's everything. Hope you found it helpful. If you have any questions, please feel free to contact me at <a href=mailto:avivyodfat@proton.me>my email</a> </p>

<p> <em> With love, <br> Aviv  </em> </p>
