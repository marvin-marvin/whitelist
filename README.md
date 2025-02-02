<p align="center">
  <img width="550" src="https://raw.githubusercontent.com/anudeepND/whitelist/master/images/logo.png">
</p>
       
       
## Commonly white listed domains for Pi-Hole (Compatible with Pi-Hole Docker Image).  
          
A robust collection of commonly white listed websites borrowed from various sources including Pi-Hole subreddit, Pi-Hole forum, Pi-Hole github repository and more!
Add these domains to your Pi-Hole setup by running a script or manually and make your setup **trouble-free!**
                
Want to report a new domain? Want to report exsisting one? Feel free to file an <a href="https://github.com/anudeepND/whitelist/issues">issue</a>.
         
         
 <p align="center">
  <img height="430" src="https://raw.githubusercontent.com/anudeepND/whitelist/master/images/run.gif">
</p> 
         
* * *
         
### Main features:
       
- The entire repo is curated.
- New domains are added frequently.
- Supports Pi-Hole Docker installation.
- Comes with a shell script i.e you can add all domains automatically at an instant.
- Domains are categorised and are included in 3 different files.
- If you are a beginner to Pi-Hole, adding these sites resolves many problems. 
       
***
     
### Description
       
The repository has 3 different files containing different domains.      
       
***whitelist.txt***       
This file contain domains that are safe to whitelist i.e it does not contain any tracking or advertising sites. Adding this file fixes many problems like YouTube watch history, videos on news sites and so on...
        
***referral-sites.txt***      
People who use services like Slickdeals and Fatwallet needs a few sites (most of  them are ads) to be whitelisted to work properly. This file contains some analytics and ad serving sites, if you don't know what these services are stay away from this list.
           
***optional-list.txt***       
This file contain domains that are needed to be whitelisted depending on the service you use. It may contain some tracking site but sometimes it's necessary to add bad domains to make a few services to work.     
          
***
           
### Installation and Usage
        
 ***For Docker installation***           
 Access you running Pi-Hole container by `docker exec -it <container-ID> bash` and proceed with the steps given below:
```
git clone https://github.com/anudeepND/whitelist.git
cd whitelist/scripts
chmod +x whitelist.sh
./whitelist.sh
```
If you keep the `/etc/pihole` on a volume outside the container you need to change `PIHOLE_LOCATION`and `GRAVITY_UPDATE_COMMAND` variables based on your setup.
         
***For whitelist.txt***     
```
git clone https://github.com/anudeepND/whitelist.git
cd whitelist/scripts
sudo chmod +x whitelist.sh
sudo ./whitelist.sh
```
             
***For referral-sites.txt***          
```
git clone https://github.com/anudeepND/whitelist.git
cd whitelist/scripts
sudo chmod +x referral.sh
sudo ./referral.sh
```

**Note: You don't have to clone the repo every time you need to update whitelist file. Navigate to `whitelist/scripts` and run it again `sudo ./whitelist.sh`**
        
***For optional-list.txt***     
You can add it manually depending upon the service you use. 
          
***     
               
### How do I determine an ad domain?
         
***Adam:ONE Assistant (Previously known as DNSthingy***
         
<a href="https://chrome.google.com/webstore/detail/adamone-assistant/fdmpekabnlekabjlimjkfmdjajnddgpc">This browser extension</a> will list all of the domains that are queried when a web page is loaded. You can often look at the list of domains and cherry pick the ones that appear to be ad-serving domains.     
        
<p align="center">
  <img width="600" height="500" src="https://raw.githubusercontent.com/anudeepND/blacklist/master/images/img1.jpeg">
</p>
      
***Using inbuilt Developer tool***     
          
For Chrome ctrl+shift+I will land you in Developer tools menu.
      
<p align="center">
  <img width="450" height="600" src="https://raw.githubusercontent.com/anudeepND/whitelist/master/images/img2.jpeg">
</p>      
          
***Using an Android app*** 
     
[Net Guard](https://play.google.com/store/apps/details?id=eu.faircode.netguard) is an Android app that can be used to monitor any specific apps, works on unrooted devices too.   
        
<p align="center">
  <img width="500" height="400" src="https://raw.githubusercontent.com/anudeepND/whitelist/master/images/img3.jpeg">
</p>
             
***
        
### Licence
```
MIT License

Copyright (c) 2019 Anudeep ND <anudeep@protonmail.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
