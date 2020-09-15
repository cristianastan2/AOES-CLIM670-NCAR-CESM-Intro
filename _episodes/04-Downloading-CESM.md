---
title: "Downloading CESM"
teaching: 0
exercises: 0 
questions:
- "How do I download CESM?"
objectives:
keypoints:
---

We will now download the model and all the setup files needed for it. These are one-time steps.

Go to your `/glade/work/` directory 
~~~
$ cd /glade/work/kpegion
~~~
{: .language-bash}

Download the CESM from Github
~~~
$ git clone –b release-cesm2.1.1 https://github.com/ESCOMP/cesm.git cesm2.1.1 
~~~
{: .language-bash}

Change to the `cesm2.1.1` directory
~~~
$ cd cesm2.1.1
~~~
{: .language-bash}

Let's take a look in that directory and talk about what is there and what is not.
Need to get the model components.

Checkout all the model components
~~~
$ ./manage_externals/checkout_externals
~~~
{: .language-bash}

Sometimes this hangs and gives an error about connecting.  If it does, try again. If it asks you a question about the certificate, you can select `p` for permanent.

Leave this running over break. 
