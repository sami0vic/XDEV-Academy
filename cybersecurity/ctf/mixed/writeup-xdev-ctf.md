---
description: 'Writeup for the #1 XDEV CTF'
---

# Writeup XDEV CTF

Firstly we visit this page: [Click Here](https://xdevlm6e.000webhostapp.com/)

<figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

After visiting the page, There is a button called Download assets.

After downloading the assets, and extracting the .rar file. I've got two files.

<figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

This is the text of the `readme.txt` file:

```
Hello there,
I hope you have already got the first flag in the page. But don't just celebrate yet, you still have got 2 flags to find:
 2- Using Cryptographic methodes, the second one can be found in "crackme.txt", good luck!
 3- by going to https://ghost-ajax.gitbook.io/xdev/cybersecurity/ctf
```

By reading the text, I know that there is a flag in the page. So, I tried to search in the source code:

<figure><img src="../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

Here we go, we've got the first flag: `XDEV{1N5P3CT_M3}`

By going back to `readme.txt` file, the second flag is in the `crackme.txt` file.

This is the text of the `crackme.txt` file:

```
"Mr. Robot" is a captivating and thought-provoking television series that premiered in 2015, created by Sam Esmail. The show revolves around the enigmatic and troubled protagonist, Elliot Alderson, brilliantly portrayed by Rami Malek. Set in the backdrop of a dystopian New York City, the series delves into the realms of hacking, corporate corruption, and the blurred lines between reality and illusion.

Elliot Alderson, a cybersecurity expert with a complex and fragmented psyche, serves as the unreliable narrator of the story. Suffering from various mental health issues, including dissociative identity disorder, Elliot is a vigilante hacker who joins an underground group known as fsociety. Led by the mysterious and charismatic Mr. Robot, played by Christian Slater, fsociety aims to take down the oppressive conglomerate E Corp, which they blame for the world's economic disparity and societal issues.

The series is renowned for its intense and suspenseful narrative, intricate plot twists, and its depiction of hacking culture. It masterfully explores RUtMQ3tGVkJfSFlMX0hfTlZWS19KWUhKUkxZfQ== themes of identity, power, and the consequences of unchecked corporate influence. The use of unreliable narration and Elliot's internal struggles add layers of complexity to the storytelling, making it a mind-bending experience for viewers.

"Mr. Robot" is visually striking, with its cinematography often mirroring the disorienting mental state of the protagonist. The series employs unique camera angles, bold compositions, and a distinctive color palette, creating a visually immersive and unsettling atmosphere.

Rami Malek's portrayal of Elliot earned him critical acclaim, including an Emmy Award for Outstanding Lead Actor in a Drama Series. Christian Slater also received praise for his role as Mr. Robot. The show's success can be attributed to its innovative storytelling, strong character development, and its willingness to tackle timely and relevant social issues.

As the series progresses, it continues to challenge viewers with its intricate narrative, moral ambiguity, and philosophical undertones. "Mr. Robot" stands out as a groundbreaking and genre-defying show that pushes the boundaries of conventional storytelling, leaving a lasting impact on the landscape of television.
```

I know that the second flag is encrypted, so I think it has no meaning.

So the encrypted flag is: `RUtMQ3tGVkJfSFlMX0hfTlZWS19KWUhKUkxZfQ==`

I think it's a `Base64` because there is `40` characters and `40 % 4 = 0` and there is `==` at the end.

After decrypting the flag using `Base64`, this is the result: `EKLC{FVB_HYL_H_NVVK_JYHJRLY}`

By analyzing this encrypted flag, it's a Caesar code:

<figure><img src="../../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

So the 2nd flag is: `XDEV{YOU_ARE_A_GOOD_CRACKER}`

Going back to `readme.txt` file, the third flag is in this page: [Click Here](https://ghost-ajax.gitbook.io/xdev/cybersecurity/ctf/mixed/1-xdev-ctf)

<figure><img src="../../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

We can know the flag by answering to: _How can you hide a page from indexing robots?_

The answer is: `robots.txt`



<figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

There is a hided page called `333.html`

By going to the hided page, we've got the third flag:

<figure><img src="../../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

The third flag is: `XDEV{HIDE_FROM_ROBOTS}`
