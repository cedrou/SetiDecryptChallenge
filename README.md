# SETI Decrypt Challenge

This repo is my answer to the [#SETIDecryptChallenge](https://twitter.com/hashtag/SETIDecryptChallenge) experiment started by [@DrReneHeller](https://twitter.com/DrReneHeller) on Twitter. 



> #SETI Decrypt Challenge. How2:https://t.co/nMq1zeQfcx, Mssg:https://t.co/URej7kfD79 @AstrobiologyNAI @SETIInstitute 
> ![ ](https://pbs.twimg.com/media/Cg98-P2WgAAk9DH?format=png)
> 
> &mdash; René Heller (@DrReneHeller) [April 26, 2016](https://twitter.com/DrReneHeller/status/724935476327624704)

Here are the files referenced in the tweet:
- The rules : [How2](SETI_rules.txt)  
- The message : [Mssg](SETI_message.txt)

This experiment leads to a paper published in 2018  
[Decryption of Messages from Extraterrestrial Intelligence Using the Power of Social Media](https://arxiv.org/abs/1706.00653)


And here is my answer to Rene Heller, sent on May 13th 2016:


> Hi
> 
> Thank you for this really fun challenge. Here is my answers, followed by a detailed solution, and a final bonus!
> 
> __ Answer __
> 
> 1. What is the typical body height of our interstellar counterparts? 2.45 m
> 2. What is their typical lifetime? 180.1 years
> 3. What is the scale of the devices they used to submit their message? 100 km
> 4. Since when have they been communicating interstellar? 10000 years
> 5. What kind of object do they live on? A telluric planet, probably a satellite of a gas giant, with an orbital of ~4M km and a low gravity.
> 6. How old is their stellar system? 6B years
> 
> 
> __ Detail __
> 
> The message is made of 1902341 binary digits and can be split into 7 chunks of 359 * 757 bits.
> 
> These chunks can be converted into binary images of 757 rows and 359 columns.
> Each chunk can be easily converted into a visible image by adding "P1 359 757 " at the beginning of each chunk and save it with the .pbm extension (Portable Bitmap Image)
> 
> Image #1: Calibration frame? The first row and the last column are 1. Everything else is 0.
>           Could be used to indicate the shape of each image (757rows x 359cols instead of 359rows x 757cols)
> 
> Image #2: 757 first natural numbers (from 0 to 756) written in base two, lsb first
> 
> Image #3: 757 first prime numbers (from 0 to 5749) written in base two, lsb first
> 
> Image #4: Sine wave picture. 
>           The first two lines of the data chunk are very large binary numbers written in base two, lsb first
>           Wave_0 = 16368191637088910834159098202685440
>           Wave_1 = 11677159761321922952849403009790256654968431476473856
>           
> Image #5: The picture shows a typical alien body.
>           The first two lines of the data chunk are very large binary numbers written in base two, lsb first.
>           Alien_0 = 60479561273104168652304174731493376
>           Alien_1 = 42037775140758923161949049149211273119409177427443712
>           
> Image #6: The picture shows the device they used to send their message. It looks like a field of antennas.
>           The first two lines of the data chunk are very large binary numbers written in base two, lsb first
>           Antennas_0 = 2468553521351190513386359178720371015680
>           Antennas_1 = 2335431952264384665006648365913340213606881670994067456
>           
> Image #5: The picture shows 4 planets with an alien close to the first, probably to indicate their planet. 
>           The second planet looks like a gas giant (we can see clouds bands), so maybe the other objects are satellites.  
>           The first two lines of the data chunk are very large binary numbers written in base two, lsb first
>           Planets_0 = 948909505053876287754040784031183263414353920
>           Planets_1 = 1401259171358630776572575392119740616658474880694279974420480
> 
> The message was broadcast in the frequency F = 452.12919 MHz, which corresponds to a wavelength L = 0.6630681285753 m.
>  
>     Wave_1 / Wave_0 =     7.134_10^17 * L =              50 ly                  (Distance from the Sun)
>    Alien_0 / Wave_0 =           3.695 * L =           2.450 m                   (Typical alien height) 
> Antennas_0 / Wave_0 =      150814.065 * L =      100000.000 m  = 100 km         (Emitting device size) 
>  Planets_0 / Wave_0 = 57972775862.651 * L = 38439899999.563 m  = 3843990 km     (Distance from the gas giant ?)
>                                                                = 0.0257 au
> 
>    Alien_1 / Wave_0 =     2.568_10^18 / F =     5.680_10^9  s = 180.1 years     (Typical alien lifespan)
> Antennas_1 / Wave_0 =     1.427_10^20 / F =     3.156_10^11 s = 10000 years     (Duration of the emission)
>  Planets_1 / Wave_0 =     8.561_10^25 / F =     1.893_10^17 s = 6_10^9 years    (Age of their stellar system)
>  
>  
> The typical alien height (2.45m) is consistent with the small gravity that could be found on a satellite 
> The distance (4M km) is also consistent with the orbit of a satellite of a giant planet.
> 
> All the numbers in the headers are expressed in the alien unit of length.
> Wave_0      Message broadcast wavelength       
> Wave_1      Distance from the sun
> Alien_0     Typical alien height 
> Alien_1     Typical alien lifespan, expressed as the distance travelled by the light during this time
> Antennas_0  Emitting device size
> Antennas_1  Duration of the emission, expressed as the distance travelled by the light during this time
> Planets_0   Distance from their gas giant
> Planets_1   Age of their star system, expressed  as the distance travelled by the light during this time
> 
> __ Bonus __
> 
> The frequency is F = 452.12919 MHz, which is (1420.4057 / Pi) MHz. 
> 
> It seems that we share some universal constant (HI line, Pi), maybe there are some others.
> So I tried to analyze their unit of length, because we have a duirect correspondance thanks to the message wavelength Wave_0.    
>     0.6630681285753 m = 16368191637088910834159098202685440 alien-meters
> 
> Therefore:
>     1 alien-meter = 4.051_10^-35 m, which is very close to the Planck Length (lP = 1.616_10^-35 m)
>     1 alien-meter = 2.506 * lP
>     
> We know that they know Pi. How 2.506, could be related to Pi ? 
>     Sqrt(2*Pi) = 2.506
>     
> So they use a unit of length which closely linked to the Planck constant (another universal constant...)
>     1 alien-meter = Sqrt(2*Pi) * lP
>     
> 
> 
> Thanks again for this fun game !  
> Cédric Rousseau
> 