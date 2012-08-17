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

I undertook this project with no budget and a team of one (me). But I didn't need a team of designers or developers to achieve my goals, since there was a technique ready-made to help me build the kind of site we wanted for our library: Responsive Web Design.

## Responsive Web Design

In 2010, Ethan Marcotte coined the name "Responsive Web Design" to describe a suite of techniques for building sites that adapt to the conditions of the user. For instance, by polling the user's device for the size of its screen and adapting the layout accordingly, Marcotte was able to build beautiful, fluid sites that looked good on any device or window size. The techniques themselves are simple. To build a responsive site you need a design based on a flexible grid, adaptable images, and CSS3 media queries. In addition, you need to let go of the need for the kind of control you thought you had building fixed-width sites and embrace the fluidity of the web.

Library websites are generally complex, sprawling things, and ours at Grand Valley is no exception. Because of this, our site doesn't work well as an example for the basics of Responsive Web Design. So before we get to how I made GVSU's library site responsive and some of the challenges libraries face, I'll walk you through the basic techniques on another site I built for the non-existent Library or Librarian (LOL) Library. You can follow along on the web at [http://lollibrary.org](http://lollibrary.org).

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

## Responsive Design at GVSU

### A Responsive Framework

### Navigation Patterns

### Responsive Forms

### Tables Won't Die

## Next Steps

## References

Allsopp, John. 2000. "The Dao of Web Design." *A List Apart*. Accessed August 16, 2012. [http://www.alistapart.com/articles/dao/](http://www.alistapart.com/articles/dao/).

Lenhart, Amanda. 2012. "Teens, Smartphones & Texting." *Pew Internet & American Life Project*. Accessed August 16, 2012. [http://www.pewinternet.org/Reports/2012/Teens-and-smartphones/Summary-of-findings.aspx](http://www.pewinternet.org/Reports/2012/Teens-and-smartphones/Summary-of-findings.aspx).

Marcotte, Ethan. 2010. "Responsive Web Design." *A List Apart*. Accessed August 16, 2012. [http://www.alistapart.com/articles/responsive-web-design/](http://www.alistapart.com/articles/responsive-web-design/).

Marcotte, Ethan. 2011. *Responsive Web Design*. New York: A Book Apart.

Mitchell, Amy, Tom Rosenstiel, and Leah Christian. 2012. "Mobile Devices and News Consumption: Some Good Signs for Journalism." *The State of the News Media 2012*. [http://stateofthemedia.org/2012/mobile-devices-and-news-consumption-some-good-signs-for-journalism/](http://stateofthemedia.org/2012/mobile-devices-and-news-consumption-some-good-signs-for-journalism/).

Pew Internet & American Life Project. 2012. "A Closer Look at Gadget Ownership." Accessed August 16, 2012. [http://pewinternet.org/Infographics/2012/A-Closer-Look-at-Gadget-Ownership.aspx](http://pewinternet.org/Infographics/2012/A-Closer-Look-at-Gadget-Ownership.aspx).

Smith, Aaron. "Cell Internet Use 2012." *Pew Internet & American Life Project*. Accessed August 16, 2012. [http://www.pewinternet.org/Reports/2012/Cell-Internet-Use-2012.aspx](http://www.pewinternet.org/Reports/2012/Cell-Internet-Use-2012.aspx).

World Bank. 2012. "Information and Communications for Development 2012: Maximizing Mobile." Accessed August 16, 2012. [http://www.worldbank.org/ict/IC4D2012](http://www.worldbank.org/ict/IC4D2012).

-------

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


[^haymobileweb]: Hay, Stephen, "There is No Mobile Web," *The Haystack*, January 7, 2011, accessed on August 16, 2012, [http://www.the-haystack.com/2011/01/07/there-is-no-mobile-web/](http://www.the-haystack.com/2011/01/07/there-is-no-mobile-web/)

[^W3CMediaQueries]: "Media Queries," *W3C*, June 19, 2012, accessed Agust 16, 2012, [http://www.w3.org/TR/css3-mediaqueries/](http://www.w3.org/TR/css3-mediaqueries/)
	
