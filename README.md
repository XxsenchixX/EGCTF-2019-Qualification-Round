# EGCTF 2019 - Qualification Round

##### Write-ups for some of the challenges from EGCTF 2019 Qualification Round.

---

#### Introduction

 I participated in [EG-CTF 2019](https://ctf2019.egcert.eg/) qualification round which was held in Friday November 15 2019 and lasted for 26 hours, These are my quick write-ups for some of the challenges. 

- Misc: QR c0d3
- Misc: SpaceX

![](https://github.com/XxsenchixX/EGCTF-2019-Qualification-Round/blob/master/IMGs/header.png?raw=true)

---

#### Misc: QR c0d3

###### Challenge Description:

```
I tried so hard and got so far but in the end I have nothing to try. Can you help me read this QR code

Flag format EGCTF{$0m3_l337_73x7}
```

###### Solution:

 We’re given an image called `QR.png`: 

![](https://github.com/XxsenchixX/EGCTF-2019-Qualification-Round/blob/master/IMGs/QR.png?raw=true)

I used [onlinebarcodereader.com](https://www.onlinebarcodereader.com/) to read the QR code, but I only got a small part of the flag:

![](https://github.com/XxsenchixX/EGCTF-2019-Qualification-Round/blob/master/IMGs/scanner.png?raw=true)

```
R_c0d3$_!$_n07_4n_34$y_74$k} 3nd_0f_Fl49 .
```

Then, I tried rotating the image by 90 degrees to see if I’ll get any different results, And voila worked:

![](https://github.com/XxsenchixX/EGCTF-2019-Qualification-Round/blob/master/IMGs/QR2.png?raw=true)

```
7h!5 m355493. Th3 fl49 !5 EGCTF{m3r9!n9_ Q
```



I kept rotating the image by 90 degrees and here is the results:

![](https://github.com/XxsenchixX/EGCTF-2019-Qualification-Round/blob/master/IMGs/QR3.png?raw=true)

```
H3ll0. Th!5 !5 4 m355493 fr0m 39yp7. Y0u n
```



![](https://github.com/XxsenchixX/EGCTF-2019-Qualification-Round/blob/master/IMGs/QR4.png?raw=true)

```
33d m0r3 7h4n 4 QR c0d3 5c4nn3r 70 d3c0d3
```



After rearranging results the final massage is:

```
H3ll0. Th!5 !5 4 m355493 fr0m 39yp7. Y0u n33d m0r3 7h4n 4 QR c0d3 5c4nn3r 70 d3c0d3 7h!5 m355493. Th3 fl49 !5 EGCTF{m3r9!n9_ QR_c0d3$_!$_n07_4n_34$y_74$k} 3nd_0f_Fl49 .
```





---





### Misc: SpaceX

###### Challenge Description:

```
Our radio station received a noise from Space. We believe it contains some messages. Can you decode it.

The flag format is: EGCTF{UPPER_CASE_TEXT_0R_NUMBER}
```

###### Solution: 

 We’re given a `mp3` file called `noise.mp3` by listening to it, I knew that it is a morse code but it sounds like it is multiple track with different frequency in the same track anyway started right away by using [morsecode.world/international/decoder/audio-decoder-adaptive.html](https://morsecode.world/international/decoder/audio-decoder-adaptive.html) to play and decode the morse code:

![](https://github.com/XxsenchixX/EGCTF-2019-Qualification-Round/blob/master/IMGs/decoder.png?raw=true)



After some researches and so much of trial and error I finally found the settings and the combinations to decode it :

![](https://github.com/XxsenchixX/EGCTF-2019-Qualification-Round/blob/master/IMGs/settings1.png?raw=true)

```
M S G 1 : E G C T F : I T W A
```



![](https://github.com/XxsenchixX/EGCTF-2019-Qualification-Round/blob/master/IMGs/settings2.png?raw=true)

```
M S G 2 : S A S E A S Y A
```



![](https://github.com/XxsenchixX/EGCTF-2019-Qualification-Round/blob/master/IMGs/settings3.png?raw=true)

```
M S G 3 : S A B C 0 R 1 2 3
```



And by combining the 3 massages the final flag is :

```
EGCTF{IT_WAS_AS_EASY_AS_ABC_0R_123}
```

