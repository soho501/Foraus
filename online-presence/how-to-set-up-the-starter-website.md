---
description: Step-by-step video & guide
---

# How to set-up the Starter Website

To support new members of the open think tank network to get a new website relatively quickly, we have developed a ‘starter think tank’ template on WordPress.

 It is available at [http://35.204.67.30/](http://35.204.67.30/) if you’d like to see what it looks like. Ponto has already installed its own version of the website, which you can see at [http://www.pontothinktank.org](http://www.pontothinktank.org)

Basic WordPress skills are highly recommended to use the starter website template. We made this template as easy to use as possible. If you are stuck at some point or need some customization to contact [it@foraus.ch](mailto:it@foraus.ch) for help. 

{% embed url="https://www.youtube.com/watch?v=kXgxaEICvOg" caption="\*A step-by.step video guide" %}

\*The video above demonstrates how to implement the starter website on wordpress; while the information below explains it in written format and includes further information.

## INSTALLING YOUR TEMPLATE

To set up your own website you need three things:

1. A domain and a hosting contract
2. A license of the Impreza theme 
3. Importing the starter website template 

### A domain and a hosting contract

It is relatively standard to purchase a domain together with a hosting contract, though this is not always the case.

A domain is a human-readable address where your website will live -- for example [www.foraus.ch](http://www.foraus.ch) or [www.polis180.org](http://www.polis180.org). Common domain providers are companies like [GoDaddy](http://www.godaddy.com) -- there might be ones that are more common in your country and who are able to sell country-specific domain names. Broadly, expect domains to cost between $10-$30 per year.

Hosting is a \(virtual\) server where the actual information and website will live. Our website template runs on [Google Cloud Platform](https://cloud.google.com/), and it is easiest for us to transfer the website to a new virtual machine \(VM\) on that platform. For data issues, we recommend that the think tanks select a server in the region where your think tank is -- for example, European think tanks should host their VMs on European servers. One of the benefits of the Google Cloud Platform is that new accounts have a $300 free usage, which should cover hosting costs for the first year. The other potential benefits to using cloud hosts is that we can scale up or reduce the resources dedicated to your website if required -- in other words there is good control over costs.

#### Setting up a host on Google Cloud

To setup a WordPress host on Google Cloud go to [https://console.cloud.google.com](https://console.cloud.google.com). Login with a Google-related account that is appropriately related to your think tank. You may need to sign up for a new Google Cloud account. Usually they will require a password but it will not incur any costs until after the free USD300 trial is over.

Once you’re logged in, you need to create a new project by clicking the drop-down on the top-left corner of Google Cloud Console. Then use the + button to add a new project. Normally, I would just call the project the same as your think tank name.

Once you have a project setup, go to the market place in the left side menu. Once there search for “wordpress bitnami”. This will display 4 options, you should choose “Wordpress Certified by Bitnami”

In the next screen, choose a deployment name \(again, it could be the same name as your think tank\) and then we recommend that you select a server in the area where you’re located \(e.g. Western Europe if that’s where you are\). Also make sure that 'allow https' is checked before you hit next.

It will take a few minutes, but on the right-hand side of the screen you should eventually get details here:  


![](https://lh6.googleusercontent.com/ZSRiYacUurGwVk7O4Ccqs3EsJgfoWAeTJBLcIAadYVPR8iiul-Zrj_5teFTBP5AOc7GsjojrmktgV9vhxzXKDU4YP8UipsqVo4YwRK3nFdYYI3Rxtk__mm7OI1-wOz1mgutXMcl4)

  
****You can grab the site address \(it should just be a series of numbers separated by dots\) and put it into a new tab on the web browser, and voila, you can log in by adding /wp-admin to the URL.

The initial user name will be “user”, and admin password is what is displayed in Google Cloud Console. ****You should create a new user for yourself and give yourself admin rights. MAKE SURE YOU SAVE YOUR PASSWORD. It does not have the ability to send email reminders unless you actively set it up.

#### Other services

If you would prefer to use a service that is not Google, that is also fine. Within Europe, we recommend [Host Europe](https://www.hosteurope.de/en/Wordpress-Hosting/). WP Basic hosting is just for 4,99€ a month. They have excellent support that can save you a lot of time if something goes wrong.

#### Connecting your domain and your hosting server

The final step once you are ready with your website is to connect your domain name to your host. To do this you will need to update the DNS settings of your domain and create an A record that points to the IP address of your host. It is difficult for us to give specific instructions in this regard, as it varies depending on the service you use.

### A license of the Impreza theme

Licenses are available at [Theme Forest](https://themeforest.net/item/impreza-retina-responsive-wordpress-theme/6434280) and cost $59. Please contact foraus or the Open Think Tank Network before purchasing as we may have licenses available.

### Importing the ‘starter website’ template

A. **Install a fresh clean Wordpress-Website**

The easiest way is a Wordpress contract with a host that provides a one-click Wordpress setup \(see above\) or by following the process outlined above on Google Cloud. Afterwards you simply need to register and login. Please don’t register your account on Wordpress.com.

B. **Install All-in-one WP Migration plugin**

Go to the ‘Plugins’ page in the administration dashboard.  
Search for the ‘All in one WP import’ plugin using the box on the top-right. Click install and then ‘Activate’.

![](https://lh4.googleusercontent.com/f6BKPSUIUZDcDZOETFW_cH5c13pqOHHepw84gR6V8QpDnSuuwGg7U6Hbdlq73VCRizRYZBWOdStB2rZRPQKqm8djos-lxt4I9y0QTMOuOC6420Nnl6MWp17eNHNnMaYcYMoRntXb)

**C. Import starter website template**

Go to All-in-one WP Migration, Go to the import tab  and upload this file:  
[https://drive.google.com/a/foraus.ch/file/d/1ViirLHv5WF3pqPGyrymcEfWQ5HfZig0d/view?usp=sharing](https://drive.google.com/a/foraus.ch/file/d/1ViirLHv5WF3pqPGyrymcEfWQ5HfZig0d/view?usp=sharing)

If you get an error, stating the file is too big you will need to do some advance configuration set-up, no worries it’s relatively easy and this will get you closer to become a badass hacker one day :

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <ol>
          <li><b>Go to you google console &gt; Computer Engine &gt; VM Instances</b>
          </li>
          <li><b>Next to your instance name click &#x201C;SSH&#x201D;</b>
            <img src="https://lh3.googleusercontent.com/ikakr1sqyDvdcFKDvwfj54tkOL0Fzs0-PiEYDRowL_Zu5JBdLapR95XXvy8y5oxdwEUqhLXgJqahdukQtHasoGCb3MYwm5LKFelnFcki5_P-BC6yGmTGwd4rbOQ0hNSUtaGgE1Pe"
            alt/>
          </li>
          <li><b>This will open a Linux Terman (how cool!)</b>
            <img src="https://lh5.googleusercontent.com/i8tQN7by_BWYR89a9DpubDJERzJGoLszgZ_UwrUmChKLMMv7G3zoGhr2Jd5Fyfp0IFXYOA6kT0_sTuzn8HtkLLpw3hcpIp8BN_d3IPd9xKkl4BpLacjxq7VbVaN5PbHu6GEOBg94"
            alt/>
          </li>
          <li><b>Now you just need to follow these instructions:</b>
            <ol>
              <li>Copy this command : sudo vi /opt/bitnami/php/etc/php.ini</li>
              <li>Use the arrow keys down till you reach the file that contains post_max_size
                = 16M</li>
              <li>Press &#x2018;i&#x2019;</li>
              <li>Now you can edit the file change the value to 300M</li>
              <li>Use the arrow key down till you reach till you reach upload_max_filesize
                = 16M</li>
              <li>change the value to 300M</li>
              <li>Press &#x2018;esc&#x2019; then &#x2018;:&#x2019; then &#x2018;w&#x2019;
                and finally &#x2018;q&#x2019;</li>
              <li>You have successfully modified the file if you are back in the console</li>
              <li>Next copy this command : sudo /opt/bitnami/ctlscript.sh restart</li>
              <li>Once everything is restarted you can close this window and go back to
                your WordPress, refresh the page and try to import the file again.</li>
            </ol>
          </li>
        </ol>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>Please note that once you import this file from back that your login will stop working. After your website has been updated you will need to login with the following information:

_**User:**_ ****dummy

_**Password:**_ &1EQBOWBOhVPvwuIxZewWLRw



**D. Contact foraus to activate the Impreza theme**

foraus purchased several instances of the Impreza theme. When you are ready, we can activate it for you. Just let us know! 

## **CUSTOMIZE YOUR WEBSITE WITH WORDPRESS**

WordPress is not a software you have to learn from scratch. You will need some workarounds to edit and add content. The best way to edit the single pages is the black toolbar on the top. Just navigate to the page you want to edit, click edit, and edit the content.

If you want to add content, the easiest way is to navigate to a similar content page, duplicate it \(Copy to new draft\), change the content and publish.

We used a visual composer to make your life easy. If you need help: [https://kb.wpbakery.com/docs/wpbakery-page-builder-how-tos/](https://kb.wpbakery.com/docs/wpbakery-page-builder-how-tos/).

### **STYLING**

To give your website your unique style you can use the Impreza Theme Options. We recommend working cautious here. Keep it simple, your content is supposed to be your star on the website.

![](https://lh4.googleusercontent.com/YOKMfs7_I6d1IjY1CN4IbponpMU7RI2qyVB_uxSOQKdDPNOokbTiN3pIe7C5FRoPqPnwFQ124lMirG0z3NyAai_zrRr9llfvW-4r5VxLw32efBn0YT0_1a6aj5NDTs3fDtyUeQo_)

#### \*\*\*\*

1.  **Colors**

The Website works with a color scheme. Default ist a black and white scheme. You can use your colors, but you should use not use too many. There a lot of color adjustment options, but we recommend: Choose a random preset scheme and change the two colors. If you don’t have own colors, choose one from the color schemes.

  **2. Typography**

Another thing you might want to change, are the fonts. You are setting can assign one font the headlines and one for regular text. The easiest is to use the same font family for both. If you would like to use one font for heading and a different one for text keep in mind that normally heading fonts are sans serif fonts and body text can be either serif or sans serif. Headings should be a ‘heavier’ version than body text.

**Don’t change anything else in the Theme Options unless you are a bit familiar with the theme.**

### **DEFAULT CONTENT TYPES**

The template is made of four default types:

1. Publications
2. Success Stories
3. Events
4. Team

#### Publications

The publications are created with categorized posts.

![](https://lh3.googleusercontent.com/78r7-Qe-0wGTD3RyLqoj0tbKoN_0VWwsSLliroaVyJzrtaJgX1AmjQDL4ggtaP3xntY9a8gWuBiZPEeJryjqvAhtVry8HDN4kZ9GorQYDPrbwm6Bc8HX-DVI8CPLRjPmVR3YH6ZE)

You can edit them and create new posts like explained above.

**If you need a new author, go to ‘Users &gt; Add New’** and give the new author a random username & email address. The role must be “Author”.

![](https://lh5.googleusercontent.com/aCdHLxl6p2bhndbbKeu-TL_CjBpSmw88KljorMrfKhH5L_NkzJ2Y7ANiZ5GbuvuXMT6l3yqAYbYZtgUjl_P_0L_GY9m6F2xKYjtqS0Yz1AWtKBnAqRYAoABUVnj4UtMAcTkHi800)

Then go to your new publication and choose the author \(at the bottom of the backend\).

![](https://lh4.googleusercontent.com/kyTya7uNAuxzItlSccp5rVuuT0Ox9VeHP1GzWAkuoISfcXZuMEh5aHC451FB7owatG2zMXlGEhFNQCKmiKy9sMfPPPqSbOlwXVIxsK7-jB_IiClWcQIbXgMfNWt1LoMKIWNJMh5O)

The author element within the publications has nothing to with this this technique. You have to edit this, too. If you need more authors, just clone the row and edit the clone:

#### Success Stories

The Success Stories are created with categorized posts. They work exactly the same as the publications.

#### Events

The events are done with a special plugin. Simply copy events to new drafts, edit and publish them. See more information about events in the Publications [content guide](../products/publications.md#events) or [organising events.](../products/1.why.md)

####  The Team

To make it easy for you adding new team members, we created a “Become a Member” button on the homepage. It’s in the “How to engage” section. If you click on it you’ll see a pop up. New members use this to register. You will get an email with that uploaded content. With this content, you can add new team members as described above.

The team items are done with the portfolio pages. Editing them works the same as publications or success stories.

You have to customize the form: go to Contact →Become a Member → Edit → Mail-Tab and edit them:

![](https://lh4.googleusercontent.com/yTls6hNHLTXSkEcnmM9FM7B3QHDgQX47bKN3W-hrhXhk7SRWyf9Axj1JjwOdRyRyDx376edEjF_z-XbXcQzB64cHITksQoYpY6pUHrumchFznVYilp_Rst7dZ212QbrURjvqRXIH)

### \*\*\*\*

### **EDITING THE HOMEPAGE**

#### 1. Content 

Click edit in the toolbar to access the homepage backend. Usually you don’t have to edit the green grids. You just need to customize your content:

To edit the row’s content, hover to the centre of the rows. A green menu appears. Green means “edit content”. Click on the pencil sign to edit. Every content type is a bit different, but it should be clear, how it works.

#### **2. Categories & Grids**

Each post can be categorized easily. We recommend creating a fixed category concept with a handful of categories \(not more than six\). This makes it easy for you and your visitors.

![](https://lh6.googleusercontent.com/kkPvggoHiDh31G-v_GEZPBiw4wtgAQmETUIiJIxYbsT0Q8CNHR5hArw4g-tjmxGGq8M0z4XRZGOzB1KjZaSXc8juTH_ktEMQTYO-Bf-3MB3qkqXSckfTD6rEZT8H8c0GVp-05k1Q)

You will find the categories in the backend → Posts → Categories. Please use the parent categories Success and Publications.

To show the Publications and Success Stories in the front-end you are using the grids.

![](https://lh6.googleusercontent.com/NONJdGszjGSeVS93bHUb_5TcbLBwlY_KUx7PQ3c8gr9CKs9DEJKMsJkVbRY-mfwt28h42t7YtBgnlYkA-ynVYVAEUKWHEL8_Qa51DX0mnjvMjIdc2RJ-ZfnLvJm9Nj5yYXfS5h40)

Please tick every category you created to show all publications. If you add a category later, you must tick it here, too.

![](https://lh4.googleusercontent.com/OkSxkwHKloj8wv1t6UZJeTS385dE4NT7CdSsspvIAEVqgaw1CmlHCQcXfSt6Is0WEF7mltNTsT3jGV1QBotFuI8f-urCXXAiCrI35tOWTGcGw9MYvizwbjQYveMqet0-RxiXReab)

You also change the number of items and and columns. We recommend, not to edit anything else here.

![](https://lh4.googleusercontent.com/7I8F_vWFOPuAwD7b5iDi5QGd_JGXWipMdnq61s33IEJ-Qh5I7C9wy2zQa3cl4LSp3nMUTVaQFEgg4aVatwp1cG97aAY18WXt5B_IQlfC_eZx4p_cVCxyKXpW5TMzIf52lMFgoUE8)

### **EDIT HEADER AND FOOTER**

Got to Impreza → Headers/Footers. The footer works the same as the other pages. The header looks a bit different, but you just need to edit the social media icons and replace the logo here. Leave everything else as it is.

![](https://lh3.googleusercontent.com/idYVnveEZPhKo8kfDdoxjLfuM_CMa71x2UgZHovnh0P9P8rk0pUMv3A4iorxqoF8gvSEiSreVgMTsDgp_4boLbdXOCtz7r75LaUgYRevf2-2588x2OzjXaxqXHvz8eIZ6rK8gdps)

![](https://lh5.googleusercontent.com/KA-qJ8IvJBedfe7NSi8lgLp_x4hgv5zwZ7j1W417Wgk5jYfbifAO8ylbGWLOulahUqVxr4PQ_6K2LXNm8JqNx13v0L8JKpM6zW9QnbqM6tRPneQ5ez3K02J6VZUsJwepQwCn1q0y)

![](https://lh3.googleusercontent.com/5Ab8q16IFjb2f5jxfrzhxa5LVcsu6g7kB0122lQ2Ok05-Z2WIUZ7b76rwNiOonWY21rY_SEfWXckzqfKetVKoa25dCIAnXHlZfoaJ3U1EWlLeySYJGbJB29wsQpGqSX0To-8rog3)

## **BACKUP AND MAINTENANCE**

You should update Wordpress, the plugins and the theme regularly to avoid hacks. Wordpress tells you if something needs to be updated. Please do a backup before updating.

**Backups:** __Updates: Go to Dashboard → All in one WP Migrations

1. Backup

2. Download and save it somewhere

**Updates:** Go to Dashboard → Updates  


  
  


  
  


