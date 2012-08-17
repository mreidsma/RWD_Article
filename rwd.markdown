At some point between the moment I am writing these words and the moment you are reading them on a printed page, this essay has been coiffed and primped by a designer for optimum readability. That designer, working in the medium of print, has at her disposal knowledge that we who make websites for a living can only dream of: she knew, with utmost certainly, the size of the book, her canvas, and made her design decisions accordingly.

If you were reading this on the web, I wouldn't be able to predict the size of the "page" you were viewing, because web-enabled devices have never looked so different. We can no longer count on one or two common screen resolutions when we start planning a website. We're on track to have more mobile devices than people on the planet (World Bank 2012), and in the U.S. nearly half of adults who own cellphones have a smartphone (Pew 2012). What's more, recent data is showing that adults who own more than one Web-enabled device is growing, with over half of computer owners also owning a smartphone and 13% of Americans owning a laptop or desktop computer, a tablet, and a smartphone (Mitchell, Rosenstiel, and Christian 2012). We have more devices with a greater variety of screens to design for than ever before.

## Giving Up Control

Web designers are just waking up to the realization that they no longer have the kind of control a print designer enjoys. But true to our desire for control, we address this problem by creating more of the same fixed-width layouts, but this time one roughly phone-shaped, another tabletish in size, and finally, the "regular" desktop site. We check for known mobile devices and browsers and send these visitors to separate websites. We Our feeling of control returns, until new phones and tablets hit the streets, requiring us to look for another dozen, or two dozen devices to make sure each device gets the appropriate website.

But the web itself has never had the kind of fixed canvas of the printed page. For the past twenty years, we have built fixed-width websites for a handful of screen sizes dictated by screen manufacturers. In the mid-nineties we made sites that were optimized for screens 480 by 640 pixels, and a few years later, we expanded to 600 by 800 pixels. In the last decade we hovered comfortably designing for screens 1024 pixels wide and 768 pixels high, and we used every inch of that canvas, because we knew the sizes of the screens our visitors had on their computers.

Except the screen was never the canvas to begin with. As Ethan Marcotte has pointed out, screen size is "one step removed from our *actual* canvas: the browser window" (2011, 3). We've never had a fixed canvas, because the users of our websites always had control of the size and shape of the browser.We've never actually had control. 

Accepting this doesn't mean that we have to abandon building beautiful sites and go back to pages of unstyled text. Long before mobile devices brought the John Allsopp pleaded with web designers to "embrace the fact that the web doesn't have the same constraints [as print], and design for this flexibility" (2000). The ability to build fluid websites has always been a part of the web, but now, a decade after Allsopp's call to arms, we have a more sophisticated arsenal of standards-based tools to make websites that adapt to changes in the user's world.

## Tackling Mobile in the Library

When I came to Grand Valley State University in late 2010, they were already trying to find a solution to the increased mobile usage of their website. That year, the GVSU Library website traffic from mobile devices was a measley .5% of all visits, while the University as a whole saw traffic from mobile devices reach 4.5% of all visits. Now just 18 months later, GVSU's library has a tenfold increase in mobile traffic. Visits from mobile devices for the first 6 months of this year hit 4.95%. That's 1 in every 20 visitors to our website using a mobile device.

As an academic library, we knew this growth will only continue. Recent studies report that a whopping 77% of teens age 12-17 have a cellphone, and 25% of those are smartphones (Lenhart 2012), and 45% of 18-29 year-old who browse the web on their phone use the phone as their primary device (Smith 2012). We needed to do something about our fixed-width website, which was barely usable on small-screen devices.

I developed a few core goals for the new site. First, all content and services would be available in full on all devices. I didn't want to make assumptions about what users on mobile devices wouldn't use. As a library, our goal is to offer the same services to all of our patrons. We would never think of limiting access to a patron in a wheel chair because we assumed they wouldn't be interested, yet it is common practice to assume that mobile users only want hours and directions. I also wanted to avoid having 2 URLs for each piece of content, one for the mobile site and one for the desktop site, which can be frustrating for multiple-device users. We would have one site, not separate mobile and desktop websites. 

I also wanted to take advantage of the capabilities of newer devices without leaving older devices or assistive technologies like screen readers from using our services. So I would build the site with clean, standards-based HTML and then enhance the site with CSS and JavaScript on more capable devices as much as possible. Like most libraries, we rely on many hosted vendor products to provide services to our patrons, so I wasn't in charge of much of the code being served to our patrons. Even though each vendor offered different levels of customization possibilities, I wanted all our disparate sites to appear to be a single, cohesive website. 

I undertook this project with no budget and a team of one (me).

Some of our goals had to be revised, since we immediately encountered some challenges that were out of our control. Like most libraries, we rely on hosted vendor projects for many of our services. As such, having a single code base was not technically possible, since many of our customizations would need to be spread over a variety of proprietary hosted interfaces that offered differing levels of customization. However, we decided to start with the campus CMS pages, since the University's website design would determine the overall look of our template. In addition, we work closely with our University's web team and had the most flexibility on making design changes.

Our first step was to implement RWD techniques on a smaller sub-website within the library to see what challenges would pop up working within the University's framework. In the spring of 2011 I started work redesigning the website for our new library usng responsive principles. [Figure] In some ways, this site was the antithesis of a library website. At only 7 pages, it was small, and it lacked many of the features we expect from typical library sites: namely, search boxes and long lists of resources. Nevertheless, I knew that many of the issues we would face in adapting a CMS site to RWD would be universal.

Our existing template used tables to structure much of the site's layout, and so I modified the template to finally move to an all-CSS layout using divs. Our webteam then loaded the library-specific CSS file after the campus-wide styles so that my styles would overwrite the existing, fixed-layout styles. For the most part this worked, although I later ran into a few issues where the base stylesheet continued to interfere with my new styles. 


## References

Allsopp, John. 2000. "The Dao of Web Design." *A List Apart*. Accessed August 16, 2012. [http://www.alistapart.com/articles/dao/](http://www.alistapart.com/articles/dao/).

Lenhart, Amanda. 2012. "Teens, Smartphones & Texting." *Pew Internet & American Life Project*. Accessed August 16, 2012. [http://www.pewinternet.org/Reports/2012/Teens-and-smartphones/Summary-of-findings.aspx](http://www.pewinternet.org/Reports/2012/Teens-and-smartphones/Summary-of-findings.aspx).

Marcotte, Ethan. 2011. *Responsive Web Design*. New York: A Book Apart.

Mitchell, Amy, Tom Rosenstiel, and Leah Christian. 2012. "Mobile Devices and News Consumption: Some Good Signs for Journalism." *The State of the News Media 2012*. [http://stateofthemedia.org/2012/mobile-devices-and-news-consumption-some-good-signs-for-journalism/](http://stateofthemedia.org/2012/mobile-devices-and-news-consumption-some-good-signs-for-journalism/).

Pew Internet & American Life Project. 2012. "A Closer Look at Gadget Ownership." Accessed August 16, 2012. [http://pewinternet.org/Infographics/2012/A-Closer-Look-at-Gadget-Ownership.aspx](http://pewinternet.org/Infographics/2012/A-Closer-Look-at-Gadget-Ownership.aspx).

Smith, Aaron. "Cell Internet Use 2012." *Pew Internet & American Life Project*. Accessed August 16, 2012. [http://www.pewinternet.org/Reports/2012/Cell-Internet-Use-2012.aspx](http://www.pewinternet.org/Reports/2012/Cell-Internet-Use-2012.aspx).

World Bank. 2012. "Information and Communications for Development 2012: Maximizing Mobile." Accessed August 16, 2012. [http://www.worldbank.org/ict/IC4D2012](http://www.worldbank.org/ict/IC4D2012).

-------




Most of the discussion about providing access to our services for mobile users centered around the most common practice at the time: detecting a user's device or browser and serving up a different, "stripped-down" version of the lbrary website to mobile devices. Libraries thus find themselves supporting two websites: the "mobile" website and the "desktop" website. (Some even support a separate "iPhone" website.) The effect is to create the perception of two different "Webs", the "Mobile Web," where efficiency rules, and the "Desktop Web," which is what everyone thinks of as the Web.

But this is just a perception. "There is no Mobile Web," Stephen Hay wrote. "There is only The Web, which we view in different ways.[^haymobileweb]" By cordoning off mobile devices into a ghettoized "Mobile Web," we convinced ourselves that people using the Web on mobile devices were doing something very different than those using the "Desktop" web. We made a lot of assumptions about web browsers and our users, in other words.

Web design has always been a little stuck in awe of the traditions of print. For many years, we web designers relied on tables to create layouts and controlled and sophisticated as print brochures. We clamored for control, and fought to have our sites look the same in every browser. But what we missed in all of this was that the fluidity and lack of control the Web offers the designer is not a bug; rather, it is a feature. As John Allsopp wrote twelve years ago," The control which designers know in the print medium, and often desire in the web medium, is simply a function of the limitation of the printed page. We should embrace the fact that the web doesn’t have the same constraints, and design for this flexibility.[^Allsopp]"

We made assumptions about mobile devices, as well. In the early ninties, a teenager like Zach Morris on Saved By the Bell using a cell phone was a punch line in a sitcom. Mobile phones were for busy professionals who were on the go and didn't have time to wait around for calls. They certainly weren't going to be someone's primary communications tool. Twenty years later, we are on track to have more activated mobile devices than people on the planet[^Worldbank]. 88% of Americans own a cell phone, and nearly half of those are smartphones.[^PewGadgets] [^PewTeens] Mobile phones are no longer a business tool for the distracted professional. They are a lifestyle tool for everyone.

But the myth of the Mobile web still encourages us to think about mobile web use as occasional use by distracted people who are on the go on a slow network. These assumptions about users are entrenched. But the data shows a more complicated picture of how people use the web on mobile devices. According to a 2012 Pew Internet report, 17% of cell phone owners connect to the web primarily or only through their phone, while 45% of 18-29 year-old who browse the web on their phone use the phone as their primary device[^PewCellUse].  

How we use our phones is different in reality as well. TK% of smartphone owners browse the web on a mobile device while home, TK% while waiting in line or during miscellaneous downtimes[SOURCE], and TK% even admit to using them in the bathroom[SOURCE]. The thing is, phones are increasingly becoming a go-to web browsing device. As libraries who strive to provide access everyone, making our services available on mobile devices is a must. Clearly we need a way out of the myth of the Mobile Web.

But we might still make use of device and browser detection without falling into the trap of the "Mobile Web," couldn't we? Perhaps, but there are other technical challenges with these methods that will be difficult to overcome. First, with countless smartphone models released every week, keeping up with such a device or browser library is unsustainable, especially for the small, perpetually understaffed library web team. In addition, this requires our small teams (or more likely, individuals) to maintain two (or three) separate code bases, even if each site offers complete functionality. 

Perhaps the most frustrating problem with this method affect users. By redirecting to a mobile version of the website, we generate multiple URLs for the same content. If a user visits our site on a mobile device to read an article and is redirected to http://m.oursite.com/article, then when they share that URL with others, everyone will be directed to the mobile version of the page. This can be frustrating to users on desktop computers, who often get a site formatted for a very different screen. Even worse, if we don't offer all of our site's functionality to the mobile site, then users on "desktop" computers find themseleves equally unable to perform tasks that were deemed unnecessary on a mobile site.

But more challenges are ahead. Many popular video game consoles available today offer robust web browsers, and SmartTVs are becoming more and more affordable. What happens when you have to maintain a mobile, a desktop, and a widescreen TV website? What about the next device that comes along that changes our assumptions about how people use the web?

There is an easier way to build sites for existing and future devices. We can maintain a single code base, making life easier for both our employees and our users, while still providing an optimal experience for any range of devices. And best of all, we can do it using good old Web standards.

## Responsive Web Design

In early 2010, Ethan Marcotte, a web designer from Boston, coined the name "Responsive Web Design" to refer to a suite of design techniques for building fluid, adaptive websites that respond to the device they are viewed on[^ALARWD]. By designing sites with fluid grids, using flexible images, and employing new CSS media queries, Marcotte was able to build websites that scaled beautifully on any screen size. 

### Fluid Grids

### Flexible Images

### Media Queries

When CSS3 came out, the existing media attribute for stylesheets was expanded. Whereas in CSS 2.1 you could declare stylesheets for screen, print, and even handheld, with CSS 3 granular attribute detection was added. Now you could serve up CSS to a screen that met certain width criteria, or was held in landscape, or even resolutions and aspect ratios[^W3CMediaQueries]. Since the techniques of determining devices and browsers were essentially trying to determine what size the screen of the device viewing the website was to serve up the optimal format, CSS width media queries were a perfect way to solve this problem without getting stuck in a race to keep up with browser versions or device models.

Media queries are added as attributes to link elements, CSS @import statements, or inline stylesheets as conditionals like the media attributes before them. For instance, here's a stylesheet that will load only if the device has a screen and the browser width is at least 600 pixels, shown in three equivalent declarations:

	<link rel="styleheet" type="text/css" href="styles.css" media="screen and (min-width:600px)" />
	@import TK

Or inside a stylesheet:

	@media screen and (min-width:600px) {
		/* Awesome styles here */
	}

This gives us a lot of flexibility on loading size-specific CSS, since we can target screen widths which will help capture a wide range of devices. But there are a few best practices we should keep in mind when writing media queries.

First, don't use pixel values for your media queries; use ems. Rather than being a fixed width measurement, ems are a relative measure that allows for user zooming without making our sites unusable. Unless you change the default body font-size in your style sheet, you can assume that by default 1em = 16 pixels. So for our previous example, instead of calling the stylesheet at 600pixels, we'll call it at 600 pixels / 16 pixels = 37.5ems. So our query would read:
	
	@media screen and (min-width: 37.5em) {
		/* Awesome styles here */
	}

Now when a user activates their browser's zoom feature, our media queries will activate based on the relative widths of the elements, or when the break points actually fail, rather than on specific widths which could activate media queries based on pixels as the browser effectively reduces pixel density of the display.

Second, write all of your media queries in a single stylesheet instead of loading separate stylesheets for each query. This reduces load times since you are only doing a single server call for your CSS instead of several.

## RWD at GVSU: 

When we started talking about implementing RWD at GVSU, we had a few core goals for the new site. First, it had to work and be usable on any device, from an 8-year-old flip phone with a bare-bones web browser to the latest tablets and laptops our students and faculty were increasingly using. We wanted a single code base based on Web standards, since our Web services staff is just me and one part-time student. We wanted it to be attractive and maybe even fun to use, and we wanted to take advantage of the capabilities of newer devices without leaving older phones and computers from accessing our services.

In addition, we wanted all of our disparate sites that are spread across different vendors to appear to be a cohesive website. With no budget, and just me making changes.

Some of our goals had to be revised, since we immediately encountered some challenges that were out of our control. Like most libraries, we rely on hosted vendor projects for many of our services. As such, having a single code base was not technically possible, since many of our customizations would need to be spread over a variety of proprietary hosted interfaces that offered differing levels of customization. However, we decided to start with the campus CMS pages, since the University's website design would determine the overall look of our template. In addition, we work closely with our University's web team and had the most flexibility on making design changes.

Our first step was to implement RWD techniques on a smaller sub-website within the library to see what challenges would pop up working within the University's framework. In the spring of 2011 I started work redesigning the website for our new library usng responsive principles. [Figure] In some ways, this site was the antithesis of a library website. At only 7 pages, it was small, and it lacked many of the features we expect from typical library sites: namely, search boxes and long lists of resources. Nevertheless, I knew that many of the issues we would face in adapting a CMS site to RWD would be universal.

Our existing template used tables to structure much of the site's layout, and so I modified the template to finally move to an all-CSS layout using divs. Our webteam then loaded the library-specific CSS file after the campus-wide styles so that my styles would overwrite the existing, fixed-layout styles. For the most part this worked, although I later ran into a few issues where the base stylesheet continued to interfere with my new styles. 

### Fluid Grids

Perhaps the most obvious and useful aspect of RWD is moving chunks of content around to make attractive and readable layouts for different screen sizes. While larger screens encourage designers to flex 


### Progressive Enhancement and "Mobile First"

Since most websites are built making assumptions about a user's browser window size, it's no surprise that many other assumptions are made about the user's device that can lead to frustration for users with less capable devices. As libraries, we wouldn't ever think of removing a handicap ramp to access our buildings because "no one in a wheelchair comes here" or "fewer than 1% of our visitors use the ramp." Our mission is to provide the same services to all of our users, regardless of how they come to us.

Yet this same inclusiveness falls away when libraries build their websites. Important considerations like HTML source order, accessibility features, and javascript fall-backs are ofte ignored simply because "not many" or "no one" is assumed to make use of them. But by overlooking these methods, we're going to shut out some users from our online services while making our jobs of building a responsive library website harder. Let me explain.

#### Source Order

The order that your HTML is presented to the user is important. In most websites designed for desktop, the source order goes something like this:  heading, navigation, content, footer. This is a pretty typical order, because on desktop sites we expect the navigation to be near the top of the page or along the left side. But when we load such a site without CSS, we are presented with a list of navigation items to other pages before we ever get to the content. Yet no one comes to your website for the navigation: they come for the content. 

When we moved from table-based layouts to CSS, we thought that by simply keeping our style attributes separate from our HTML we were separating style from structure. But we continued to put the navigation at the top of our document structure since that's where we expected it to appear on the page. By moving navigation below our content, we can improve the experience less-capable devices have visiting our sites and use CSS to progressively enhance the site for devices that have CSS capable browsers. When coupled with media queries, we can easily move the navigation visually to the top of the page with CSS. 

### Navigation patterns

This was one of the first issues I had to address with our site: where would the navigation live, and how would it look on different screen sizes? I was able to convince our University web team to move the navigation below the content, which was the opposite of the existing template. But I was able to keep the existing look of the left-side navigation on large screens by floating the content and navigation right instead of the default left. 

That means that on small screens, I don't have to do much at all to change the navigation. I want it to fall below the content, which it already does in the source order, so I simply need to style it. In our case, I made the decision to use the existing CMS template navigation styles since our users are accustomed to them on GVSU websites. I simply modified a few of the CSS attrbutes to allow them to behave like the rest of the columns in our layout, specifying widths as percentages instead of pixels.

One problem, however, is how to let mobile users know that the navigation has moved to the bottom of the screen and to keep them from having to scroll all the way below the content if they do need to navigate to another page. This is solved most easily by adding an id to the navigation wrapper and adding an anchor link before the content. The markup on our current site looks like this:

	<div id="gvsu-library_menu"><a href="#navigation">Menu</a></div>

	... Content goes here ...

	<div id="navigation">

	... Navigation goes here

For small screens we can style the link appropriately and then hide it on wider screens when the navigation is at the top. In our case, I wanted hide the text and use the same icon our campus used for their responsive homepage. I hid the text by moving it far off the screen an used a CSS background image. While you could use an image in the markup instead of the text, this would not be as useful for less capable seizes where CSS was not available or for screen readers that rely on text to help visually impaired users navigate websites. The CSS looks like this:

	#gvsu-library_menu {
		background: transparent url(img/menu.png) top left no-repeat;
		text-indent: -9999px;
	}

	#navigation {
		float: none;
		width: 100%;
	}

	@media screen and (min-width: 48em) {
		
		#gvsu-library_menu {
			display: none;
		}

		#navigation {
			float: right;
			width: 22%;
		}


This solution is simple and relies only on 



 

JavaScript has gotten a bad rap over the past decade, but it's an important tool for building and customizing sophisticated front-end experiences for our users. One of the main reasons it has gotten such a bad rap in the past is 


## Thinking big: campus-wide RWD

## GVSU Library website goes responsive


RWD at GVSU
Goals for the site: usable on any device, attractive (and maybe fun) on more capable devices
Challenge: library website was not a cohesive site. Code base largely dictated by outside influences: hosted vendor sites (Summon, 360 Link, EZProxy login, Illiad, Ares), campus CMS (custom), library=specific tools (Library Labs, Instruction Menu) - make them all look and work uniformly on all devices. With no budget and just me.
First step: test the waters of the CMS
Build the Mary I promotional site inside the CMS to see what can be done. 
	Challenges: default non-responsive styles from campus. 2 approaches: overwrite AND remove with JS - other people's templates
	Benefits: small, contained, targeted site with single code base.
* Navigation patterns
Thinking big: Campus moves to responsive design
Waiting.
Now only CMS content needs to use our styles: template is already responsive!
Challenges: content, tables, consitency
* Your website has too much crap.
* Designing a flexible grid system
* RWD patterns for tables

Vendor websites
Challenges: unlikely to convince a vendor to move in this direction
* Vendors that give you nearly complete control (Illiad)
* Vendors that give you some access to branding but use tables for layout: do your best and then employ javascript to enhance capable devices  (360Link Reset)
* Vendors that don't give you much control
* Vendors that do device or browser detection that you can't control (Summon, LibGuides)
* The response: library website hasn't been live long enough to get quantitative data, but in my experience there is no a-ha moment: this is what your users expect. No one pats you on the back when you meet basic expectations.

FOOTNOTE: 1. Firstname Lastname, “Title of Web Page,” Publishing Organization or Name of Website in Italics, publication date and/or access date if available, URL.

REFERENCE: Lastname, Firstname. “Title of Web Page.” Publishing Organization or Name of Website in Italics. Publication date and/or access date if available. URL.

Horrigan, John. A Typology of Information and Communication Technology Users. Pew Internet & American Life Project, May 6, 2007, http://www.pewinternet.org/PPF/r/213/report_display.asp, accessed on May 10, 2007.

[^haymobileweb]: Hay, Stephen, "There is No Mobile Web," *The Haystack*, January 7, 2011, accessed on August 16, 2012, [http://www.the-haystack.com/2011/01/07/there-is-no-mobile-web/](http://www.the-haystack.com/2011/01/07/there-is-no-mobile-web/)

[^Allsopp]: Allsopp, John, "The Dao of Web Design," *A List Apart*, April 7, 2000, accessed August 16, 2012, [http://www.alistapart.com/articles/dao/](http://www.alistapart.com/articles/dao/)


[^PewTeens]: Lenhart, Amanda, "Teens, Smartphones & Texting," *Pew Internet & American Life Project*, March 19, 2012, access August 16, 2012, [http://www.pewinternet.org/Reports/2012/Teens-and-smartphones/Summary-of-findings.aspx](http://www.pewinternet.org/Reports/2012/Teens-and-smartphones/Summary-of-findings.aspx)

[^PewCellUse]: Smith, Aaron, "Cell Internet Use 2012," *Pew Internet & American Life Project*, June 26, 2012, accessed August 16, 2012, [http://www.pewinternet.org/Reports/2012/Cell-Internet-Use-2012.aspx](http://www.pewinternet.org/Reports/2012/Cell-Internet-Use-2012.aspx)

[^ALARWD]: Marcotte, Ethan, "Responsive Web Design," *A List Apart*, May 25, 2010, accessed August 16, 2012, [http://www.alistapart.com/articles/responsive-web-design/](http://www.alistapart.com/articles/responsive-web-design/)

[^W3CMediaQueries]: "Media Queries," *W3C*, June 19, 2012, accessed Agust 16, 2012, [http://www.w3.org/TR/css3-mediaqueries/](http://www.w3.org/TR/css3-mediaqueries/)

Marcotte, Ethan. 2011. *Responsive Web Design*. New York: A Book Apart.

Mitchell, Amy, Tom Rosenstiel, and Leah Christian. 2012. "Mobile Devices and News Consumption: Some Good Signs for Journalism." *The State of the News Media 2012*. http://stateofthemedia.org/2012/mobile-devices-and-news-consumption-some-good-signs-for-journalism/
	
