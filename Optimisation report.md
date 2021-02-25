# Optimisation Report for GoMike Designs


## Intro
As discussed, I have completed an audit and optimisation of the home and contact pages of the site, focusing on accessibility and SEO improvements. I also corrected a few coding errors as well. This report will cover the results of the inital audit and Lighthouse report, document all alterations made to the code and the improvements shown in the secondary Lighthouse report.

## Initial Audit
A google Lighthouse report of the initial code provided resulted in the following scores:

**Homepage** View [here](https://github.com/htamlyn/oc-project4/blob/master/Lighthouse%20Report%20Pre%20homepg.pdf)
* Performance - 66
* Accessibility - 87
* Best Practices - 86
* SEO - 94

**Contact Page** View [here](https://github.com/htamlyn/oc-project4/blob/master/Lighthouse%20Report%20Pre%20pg2.pdf)
* Performance - 99
* Accesibility - 58
* Best Practices - 86
* SEO - 81

From the results of the reports and additional guidance from WCAG guidelines and Google SEO Documentation, a list of 18 key points to be altered were identified (7 accessibility, 9 SEO and 2 overlapping).
The full results of the initial audit can be downloaded [here](https://github.com/htamlyn/oc-project4/blob/master/Initial%20audit.xlsx)


## Alterations Made

* Alteration Made
  * Justification from audit

### Accesibility Adjustments
* Text color altered from  to  to increase contrast
  * A low text contrast ratio makes text harder to read
* <lang> value of en altered from default
  * Screen readers need the language specified to read accurately
* Aria-labels added to <a>
  * Links using icons need to have labels for assistive technology
* <label for=""> syntax added to forms
  * Forms rquire labels to be read by assistive technology
* Various <div> elements altered to <main>, <header>, <section>, <article>, <aside> and <footer>
  * Use of semantic markup makes pages easier to read for assistive tech
* Font size of smaller text increased to minimum of 16px (12pt)
  * Body text needs to be large enough to be perceivable to users
* Navigation links in header renamed to Contact instead of page2, additional hover effects added to change the color
  * Navigation Links need to easily understandable and have focus emphasis

### Overlapping Adjustments
* Alternative text for images - removed list of keywords and created description of the image using keywords where possible
  * Images require adequate descriptive alternative text, use of keywords also improves SEO
* Altered heading structure to remove excess <h1> and ensure logical descending order over the page
  * Appropriate heading structure improves crawlability and accesible technology 

### SEO Adjustments
* Improved the description <meta> to accurately describe the page and its function
  * The meta description tag is shown on the search page and shoud be a page summary
* Removed the keywords <meta> and span containing keywords in tiny font
  * Keywords tag is outdated, and lists of keywords in tiny font risks penalisation from google
* Altered the images and quotes put in as titles to <h2> or <aside> elements to improve responsive performance
  * Google operates on a mobile first system, so how the site runs in mobile sizing is crucial
* Change contact link in bloc-3 to a button and increased spacing in footer to ensure tap target size
  * Tap targets need to be of an appropriate size 
* Compressed and formatted images to WebP to drastically reduce load and improve performance
  * Images need to be appropriately sized on the page
  * Images need to be in an appropriate format to increase performance and SEO
* Minified all JS and CSS Files (originals kept aside for ease of maintenance)
  * Minifying your code reduces file size and improves performance
* Altered page titles to be unique and descriptive
  * The title of the page should tell the user the topic of the page
* Altered some link text to be more obvious and removed excess SEO links from footer, hover effects added to footer links
  * Links are cruicial to crawlability and need appropriate text as well being clearly a link. External links are important but too many irrelevant links alerts    spam and becomes unproductive

### Additional Adjustments
* Initially page 2 was not formatting correcrtly as the scripts referenced incorrect files - fixed
* Fixed a few small spelling errors


## Post Adjustments Lighthouse Report
After all the adjustments Lighthouse reports showed the following scores:

**Homepage** View [here](https://github.com/htamlyn/oc-project4/blob/master/Lighthouse%20Report%20post%20homepg.pdf)
* Performance - 82 (from 66)
* Accessibility - 97 (from 87)
* Best Practices - 86 (from 86)
* SEO - 100 (from 94)

**Contact Page** View [here](https://github.com/htamlyn/oc-project4/blob/master/Lightouse%20Report%20post%20pg2.pdf)
* Performance - 75 (from 99)
* Accesibility - 98 (from 58)
* Best Practices - 86 (from 86)
* SEO - 100 (from 81)

As can be seen with regards to accesbility and SEO these are marked improvements, with google having no more SEO recommendations. The best practices section had no alterations as the main issues flagged here is the use of JS libraries, which at this point I could not change but may be something to be looked at in the future. Although performance was significantly increased in the homepage, it did decrease in the contact page. However this was due to the fact that before the page was not formatting and several elements were not being loaded at all, thus improving its speed, naturally once it formatted properly this reduced but 75 is still a good score. I would recommend reviewing some of the pictures to further improve performance as compression can only do so much and re-formatting at the source would help to further reduce their size.





