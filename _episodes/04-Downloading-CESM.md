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
$ cd /glade/work/cstan
~~~
{: .language-bash}

Download the CESM from Github
~~~
$ git clone -b release-cesm2.1.5 https://github.com/ESCOMP/cesm.git cesm2.1.5 
~~~
{: .language-bash}

Change to the `cesm2.1.5` directory
~~~
$ cd cesm2.1.5
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

~~~
> ## Warning
>
> If a problem was encountered during checkout_externals, which may happen with an older version of the svn client software, it may appear to have downloaded successfully, but in fact only a partial checkout has occurred.
~~~
>
{: .callout}

To confirm a successful download of all components, you can run checkout_externals with the status flag to show the status of the externals:

~~~
./manage_externals/checkout_externals -S
~~~
{: .language-bash}

This should show a clean status for all externals, with no characters in the first two columns of output, as in this example:

~~~
Processing externals description file : Externals.cfg
Processing externals description file : Externals_CLM.cfg
Processing externals description file : Externals_POP.cfg
Processing externals description file : Externals_CISM.cfg
Checking status of externals: clm, fates, ptclm, mosart, ww3, cime, cice, pop, cvmix, marbl, cism, source_cism, rtm, cam,
    ./cime
    ./components/cam
    ./components/cice
    ./components/cism
    ./components/cism/source_cism
    ./components/clm
    ./components/clm/src/fates
    ./components/clm/tools/PTCLM
    ./components/mosart
    ./components/pop
    ./components/pop/externals/CVMix
    ./components/pop/externals/MARBL
    ./components/rtm
    ./components/ww3
~~~
{: .output}

Leave this running over break. 
