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

I undertook this project with no budget and a team of one (me). It took about a week.

## Responsive Web Design

In my work with clients I had already embraced 

### Mobile First

In the past, I started all of my Web design projects in Photoshop or the browser, putting together mockups of a site that would be a fixed, desktop width. But because a larger percentage of my own personal browsing is done on a mobile device, I've started thinking differently about how I struture and build websites. Rather than starting with a vision of the site on a large screen and then stripping away features or styles as the screen size drops, I now start with the smallest screen as my base and then add styles to change the layout for devices with wider screens. 

And this doesn't just affect how I write CSS. The order that your HTML is presented to the user is important. In most websites designed for desktop, the source order goes something like this:  heading, navigation, content, footer. This is a pretty typical order, because on desktop sites we expect the navigation to be near the top of the page or along the left side. But when we load such a site without CSS, we are presented with a list of navigation items to other pages before we ever get to the content. Yet no one comes to your website for the navigation: they come for the content. 

When we moved from table-based layouts to CSS, we thought that by simply keeping our style attributes separate from our HTML we were separating style from structure. But we continued to put the navigation at the top of our document structure since that's where we expected it to appear on the page. By moving navigation below our content, we can improve the experience less-capable and assistive devices have visiting our sites and use CSS to progressively enhance the site for devices that have CSS capable browsers. In fact, Marcotte has recently been proposing that Web designers think of layout itself as an enhancement (Wroblewski 2012).

So began with an HTML source order that looked like this: heading, library search, content, navigation, footer. This document structure now presented our content in the order it was used by our patrons. Most visits result in a search of our single search box. After that, people want to access our content. And finally, they want to find other pages on our site.

To begin work on the CSS for the GVSU University Libraries website, then, did a lot of drawing on paper. Photoshop was great for building static, fixed-width mockups, but I find that paper is a better tool for capturing the fluid nature of I shrunk my browser window to as narrow as it would go and started making changes to the CSS. I find that getting my ideas into working code as fast as possible using actual site content works better than playing with static mockups. You can follow along on the live site at [http://gvsu.edu/library](http://gvsu.edu/library). If you don't have a mobile device, make your browser window as narrow to simulate a small-screen device.

At assist with the rapid development of new projects, I created a User Interface Pattern Library, which is essentially a CSS library that gives me a head start on the common design patterns we use throughout our Web projects. By including these styles, I no longer had to worry about styling typography or lists. You can see our reference document or grab the code for our pattern library at [http://gvsu.edu/library/ui](http://gvsu.edu/library/ui). 

Since I'm working initially with a narrow screen, I treat each chunk of content as a block element, and not much needed to be done outside of typography and list styles. However, navigation posed some special challenges. I had moved the navigation below the content, but to get to it mobile users have to scroll to the bottom of the page. I needed a way to give users who needed to get right to the navigation a quick way to access it without interfering with the content of the page. The simple solution we are using for now is to add an anchor link in the markup after the header that jumps the user down to navigation. The markup looks like this:

	<div id="gvsu-library_menu"><a href="#navigation">Menu</a></div>

	...

	<div id="navigation">
		<ul>
		...

In the end, I wanted to style the link to match the navigation icon used by our campus homepage. But I prefer not to use an image in the markup as a link, even with alt and titles tags. So I used the text, "Menu" for less-capable devices and then hid it from view and used a CSS background image for the navigation icon on more capable browsers. The markup for the menu link looks like this:

	#gvsu-library_menu a {
		text-indent: -9999px;
		background-image: transparent url(img/mobile_dropdown.gif) top left no-repeat;
	}

Now the page is looking pretty good on small screens , but as I make the browser window wider, it starts to look less inviting. In fact, once the browser window gets beyond 800 pixels, the site starts to look silly [Figure 4]. I needed a way to enhance the layout as the screen size increased.

### Media Queries

If you've been writing CSS for a while, you are probably familiar with the media attribute that has been around for a few years. This allowed you to make some of your styles conditional based on the type of device the page was loading on. You could have separate styles for screens, for projectors, and for print. You could even specify a stylesheet for "handheld," but support was nearly non-existent in early mobile browsers.

The CSS3 specification pushed these media attributes farther, creating a way to check in with devices to see if certain conditions were being met. Now instead of serving the same CSS to all screens, for instance, you can specify a subset of CSS to be loading on screens of a certain width or aspect ratio. To build a responsive site, we need to adapt our layouts to the width of the user's screen.

Media queries are added as attributes to link elements, CSS @import statements, or inline stylesheets as conditionals like the media attributes before them. For instance, here is a block of CSS that will only be applied to screens that are at least 600 pixels wide:

	@media screen and (min-width:600px) {
		/* Awesome styles here */
	}

This gives us a lot of flexibility on loading size-specific CSS, since we can target screen widths which will help capture a wide range of devices. But pixel values in media queries have some drawbacks. A better solution would be to set our queries against ems. Rather than being a fixed width measurement, ems are a relative measure that allows for user zooming. Unless you change the default body font-size in your style sheet, you can assume that by default 1em = 16 pixels. To convert pixels to ems, just divide the desired pixel width by the pixel equivalent of an em. In this case, instead of calling the stylesheet at 600 pixels, we'll call it at 37.5 ems (600 ÷ 16 = 37.5). So our query would read:
	
	@media screen and (min-width: 37.5em) {
		/* Awesome styles here */
	}

Now we have a mechanism to load styles based on particular widths, but I still need to figure out how these elements are going to be displayed on larger screens. For that, I need to develop a grid.

### Fluid Grids

Designing your site on a grid is a good idea, whether your site is fixed-width of responsive. Grids can, to some extent, give us some of the control we loved about table-based layouts, where items were placed logically in columns and rows. Grids are, after all, systems "for ordering graphical elements of text and images" (Boulton 2005), but unlike tables, which reproduce inflexible grids in markup, our grids will simply guide us as we place our content on the page.

Since our campus CMS dictated much of our template design, I took many of their existing design elements into account as I developed the grid that would underlie the University Libraries website. Our University's web team recently redesigned the campus homepage to be responsive, and so much of the grid that they had developed would set up the constraints of the grid I would adapt for library use.

To explain this, it makes more sense to work from a large screen down. On a large screen, the content of the University Libraries site is wrapped in a container 976 pixels wide, divided into four equal columns [Figure 1]. So by dividing our total page width by four, we can begin to build our grid.

	976 ÷ 4 = 244

Each of our columns will be 244 pixels wide [Figure 2]. But remember that our navigation comes in the HTML source *after* all of the content, meaning that we'll have to think of the content of the site in terms of three columns instead of four, while the navigation will serve as the stand-in fourth column. Here is the markup:
	
	<div id="wrapper">

		<div class="line">
			<div class="column">
				<h3>Find</h3>
				...
			</div>
			<div class="column">
				<h3>Services</h3>
				...
			</div>
			<div class="column">
				<h3>Today's Hours</h3>
				...
			</div>
		</div><!-- End .line -->

		<div class="line">
			...
		</div>

		...

		<div id="navigation">
			...
		</div>
	</div>

	#wrapper {
		margin: 0 auto;
		width: 976px;
	}

	.line {
		float: right;
		width: 732px;
	}

	.column {
		float: left;
		width: 244px;
	}

	#navigation {
		float: right;
		width: 244px;
	}

This works well for our site on large screens such as desktops or laptops, but the fixed-width layout gives us some problems on smaller screens or browser windows. But we don't have to give up our grid in order to make the page respond more gracefully to the widths of our users' screens. Instead, we can convert our pixel-based layouts to fluid, relative values using percentages. And we have everything we need in the markup above.

Since each column is a child of the .line element, we simply need to know what percentage of the .line element each column should be. If we divide the desired width of our element by the width of the containing element, we can get the relative width of our elements expressed as a percentage. So for the markup above, when we divide the width of the column by the width of its container (.line) and multiply by 100, we get the relative width of each column:

	(244 ÷ 732) * 100 = 33.333333333333%

So we can change our CSS to

	.column {
		float: left;
		width: 33.333333333333%;
	}

The navigation column, however, is a child of the #wrapper div, so we need a different value for the relative width of this column:

	(244 ÷ 976) * 100 = 25%

So we can change our CSS to

	#navigation {
		width: 25%;
	}

We can calculate the relative width of the .line container in the same way, by dividing its value in relation to the parent element:

	(732÷ 976) * 100 = 75%

So we can change our CSS to

	.line {
		float: right;
		width: 75%;
	}

But we are still left with a fixed container, so our relative widths don't adjust to changes in screen size, since their container is a fixed width. But determining the relative width of the outermost containing element is tricky, because you don't actually *know* what the width of the element containing this element is. Nonetheless, we can use some guesswork and trial and error to find an appropriate value.

One way to do this is to look at your existing analytics and determine what different screen sizes commonly visit your site. We're not going to necessarily lock ourselves in to making a site that targets one specific width, but you can use this information to help you better understand what relative size your outermost containing element should be. For instance, if 50% of your large-screen visits come from screens 1024 pixels wide and the other half come from screens 1200 pixels wide, you can use the formula above to find the percentages your .line div would be for each of those containers.

	(976 ÷ 1024) * 100 = 95.3125%
	(976 ÷ 1200) * 100 = 81.333333333333%

Since in this hypothetical case, our audience is split evenly between these two options, we could take the average of the two values and make our .line 88.3229165%, but we might also us this as a starting place to try out a few resolutions and see what works best. In this case, 88% works pretty well on both screen sizes, so we can change our CSS now to read:

	#wrapper {
		margin: 0 auto;
		width: 88%;
	}


Now our four-column layout is flexible, adjusting to differences in screen sizes. But the previous example left out something important in calculating layouts: margins and padding. When calculating the relative widths of elements, determining the containing element was straightforward. But for margins and padding are a different beast. For margins, divide the desired width of the margin by the width of the element's container. If we wanted each column to have a 6 pixel left margin, we would divide the margin width by the expected width of the .line, which is the containing element:

	(6 ÷ 732) * 100 = 0.819672131148%

There is no need to round these results, since computers are more comfortable than we are with complex numbers.

For padding, you need to divide the desired width of padding by the width of the element itself, not its container. For instance, if we want to add 6 pixels of horizontal padding to each column in our layout, we would divide the desired pixel width by the width of .column:

	(6 ÷ 244) * 100 = 2.459016393443%

But because the padding is added to the width of the element, we need to remove the same relative amount from our width element to accommodate the padding. So our CSS would now look like this:

	.column {
		float: left;
		margin-left: 0.819672131148%;
		padding: 0 2.459016393443%;
		width: 22.540983606557%;
	}

Now we have a nice, flexible four-column layout that looks great on wider screens. But even though we've built a flexible grid under our design, things start to look cramped at smaller screen sizes [Figure 3]. I need to understand where to load this different CSS.

One common practice for determining break points for layouts is to map them to common devices. We might make some changes at 480 pixels, the width of the iPhone in landscape mode, and some more at 600 pixels, the width of a Kindle Fire in portrait. Of course, we'll have something at 768 pixels and 1024 pixels, because of the iPad in portrait and landscape. But if the years we spend building device-specific websites has taught us anything, it's that locking our designs to specific devices is unsustainable. Already, the iPad 3rd generation with its high-resolution screen is throwing off proponents of fixed, device-centric break points. The best way to determine an appropriate break point is by mapping it to your actual content, and this is going to involve some trial and error.

At our smallest size, I have a single column website, while at the largest size, I want to have four columns. 


### Flexible Images


## Further Challenges

## User Response


## References

Allsopp, John. 2000. "The Dao of Web Design." *A List Apart*. Accessed August 16, 2012. [http://www.alistapart.com/articles/dao/](http://www.alistapart.com/articles/dao/).

Boulton, Mark. 2005. "Five simple steps to designing grid systems – Preface." Accessed August 17, 2012. [http://www.markboulton.co.uk/journal/comments/five-simple-steps-to-designing-grid-systems-preface](http://www.markboulton.co.uk/journal/comments/five-simple-steps-to-designing-grid-systems-preface).

Lenhart, Amanda. 2012. "Teens, Smartphones & Texting." *Pew Internet & American Life Project*. Accessed August 16, 2012. [http://www.pewinternet.org/Reports/2012/Teens-and-smartphones/Summary-of-findings.aspx](http://www.pewinternet.org/Reports/2012/Teens-and-smartphones/Summary-of-findings.aspx).

Marcotte, Ethan. 2010. "Responsive Web Design." *A List Apart*. Accessed August 16, 2012. [http://www.alistapart.com/articles/responsive-web-design/](http://www.alistapart.com/articles/responsive-web-design/).

Marcotte, Ethan. 2011. *Responsive Web Design*. New York: A Book Apart.

Mitchell, Amy, Tom Rosenstiel, and Leah Christian. 2012. "Mobile Devices and News Consumption: Some Good Signs for Journalism." *The State of the News Media 2012*. [http://stateofthemedia.org/2012/mobile-devices-and-news-consumption-some-good-signs-for-journalism/](http://stateofthemedia.org/2012/mobile-devices-and-news-consumption-some-good-signs-for-journalism/).

Pew Internet & American Life Project. 2012. "A Closer Look at Gadget Ownership." Accessed August 16, 2012. [http://pewinternet.org/Infographics/2012/A-Closer-Look-at-Gadget-Ownership.aspx](http://pewinternet.org/Infographics/2012/A-Closer-Look-at-Gadget-Ownership.aspx).

Smith, Aaron. "Cell Internet Use 2012." *Pew Internet & American Life Project*. Accessed August 16, 2012. [http://www.pewinternet.org/Reports/2012/Cell-Internet-Use-2012.aspx](http://www.pewinternet.org/Reports/2012/Cell-Internet-Use-2012.aspx).

World Bank. 2012. "Information and Communications for Development 2012: Maximizing Mobile." Accessed August 16, 2012. [http://www.worldbank.org/ict/IC4D2012](http://www.worldbank.org/ict/IC4D2012).

Wroblewski, Luke. 2012. "An Event Apart: Rolling Up Our Responsive Sleeves." Accessed August 17, 2012. [http://www.lukew.com/ff/entry.asp?1494](http://www.lukew.com/ff/entry.asp?1494)

-------




[^haymobileweb]: Hay, Stephen, "There is No Mobile Web," *The Haystack*, January 7, 2011, accessed on August 16, 2012, [http://www.the-haystack.com/2011/01/07/there-is-no-mobile-web/](http://www.the-haystack.com/2011/01/07/there-is-no-mobile-web/)

[^W3CMediaQueries]: "Media Queries," *W3C*, June 19, 2012, accessed Agust 16, 2012, [http://www.w3.org/TR/css3-mediaqueries/](http://www.w3.org/TR/css3-mediaqueries/)
	
