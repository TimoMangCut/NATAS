1/ Natas 0:

Hint is a joke. If we logged in next level, it’ll show password of that level. :D

![](Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.001.png)

Okey, first view source to check

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.002.png)


Password is here

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.003.png)

2/ Natas 1:

Right click was blocked, use Ctrl + U to view source

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.004.png)

Password is here too

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.005.png)

3/ Natas 2 :

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.006.png)

View source again, see a path to image? Click to view

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.007.png)

Nothing, try to access files

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.008.png)

See users’s file. View

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.009.png)

Password is here

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.010.png)

4/ Natas 3 :

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.011.png)

Again, check source

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.012.png)

Nothing is here, try to scan directory. But a file usually have in ctf is ‘robots.txt’

Access robots.txt, see a path to dis-allow bot

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.013.png)

Access /s3cr3t/

See a files users, password is in there

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.014.png)

5/ Natas4 :

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.015.png)

Hint : We can not access this page because we didn’t come from next level.

In htpp-header has a header is ‘referer’, Web server read this header can understand that this request come from where.

Use Burp-Suite, add ‘referer’ with a url of natas5.

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.016.png)

View Response, Access was granted.

6/ Natas5 :

This page block to access because I am not logged in, but here is nothing log-in function.

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.017.png)

Use Burp-Suite to intercept and view each request. See a field loggedin in header cookie = 0, It’s mean false, change it to ‘1’ = true and forward.

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.018.png)

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.019.png)

7/ Natas 6:

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.020.png)

View source to view code.

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.021.png)

Here is include a another file code, to check input is it equal with $secret in file code was included.

Try to access this path. See secret

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.022.png)

Enter secret

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.023.png)

8/ Natas7 :

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.024.png)

View source, nothing is here but see a hint, like a path to view password.

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.025.png)

Use function of web page, see in url taskbar, guess this web GET a input for parameter ‘page’.

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.026.png)

Try to change this path to a path in hint.

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.027.png)

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.028.png)

9/ Natas 8 :

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.029.png)

View source code, See that a webserver get a POST request to check that input equal to $encodedSecret ?

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.030.png)

Use VSCode to decode this Secret

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.031.png)

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.032.png)

10/ Natas 9 :

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.033.png)

View source code, see that get a request to call a system execute.

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.034.png)

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.035.png)

Use ‘;’ to explode each command

The command will like this : `grep -i a; cat /etc/natas\_webpass/natas10 ; dictionary.txt`

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.036.png)

11/ Natas 10 :

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.037.png)

View source, ‘ &, | , ; ‘ was block by regular expression

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.038.png)
![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.039.png)

Try to use ‘\n’ to explode each command 

![](./images/Aspose.Words.ec96a0d2-59ec-4c0b-92e6-a5249ce82cc1.040.png)
