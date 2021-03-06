# Footprints Extension
A Chrome extension written for Northwestern IT to extend the functionality of the Footprints IT Service Manager.

## Aesthetic Changes

### Card Layout
Creates a more modern, card based layout out of the tickets homepage. Issues should be much more readable and pleasant to look at. Each
separate ticket is now a card. The UI functions much the same as the original page, albeit only displaying critical information on first glance.
The ticket number in the bottom left is colored based on issue status, and it can be clicked to copy the ticket number.

![Cards](../media/Cards.png?raw=true)

### New Favicon
Since TSC Tier 1 is required to use this extension, we tried to give as many hints as possible that the extension is installed
so that it is more evident if ever it is *not* installed. Accordingly, a new favicon was designed for Footprints to match Northwestern's
purple theme. When the extension is installed, the favicon in the browser looks like this:

![New Favicon](https://i.imgur.com/Yd4JlvG.jpg)

## Features
This extension provides a number of features that improve the experience of using Footprints.

### Location Detection (TSC Tier 1 Only)
Tier 1 of the IT Support Center is required to set the **Location** field on all tickets that we complete.
To streamline this process, the extension uses the subnet of the computer that it is currently running on to determine
whether the user is at our 1800 Sherman location or our University Library location and it automatically sets the location
accordingly on all tickets created or edited during that session.

In the event that the location cannot be accurately determined (for example, if the user is on the wireless network), a warning
is shown that a location has not been automatically selected, and the location can be set manually through the menu under the
extension's icon.

![Footprints Location Warning](https://imgur.com/PKQl2JJ.jpg)

![Footprints Extension Menu](https://imgur.com/ivkXhRO.jpg)

**For non-Tier 1 users of the extension**, we recommend that you turn off the location features in the
[extension settings](chrome://extensions/?options=bhcajiiignledggebpaalkpcccbjohhc). This will disable the warning and it will
stop the extension from automatically setting the Location field.

### Conweb Interaction (TSC Tier 1 Only)
[Conweb](https://kb.northwestern.edu/internal/conweb) will display a warning by default that this extension is not installed.
Once this extension is installed and Conweb is refreshed, the message will be removed.

![Conweb](https://imgur.com/jHcptxW.jpg)

### Category Search
Since Footprints has [nearly 1000](https://kb.northwestern.edu/internal/87181) distinct categories, it can be difficult to
remember where all of them are or even to know that some of them exist. This extension provides a method of searching for
categories and displaying the closest matching ones.

![Category Search](https://imgur.com/WJ2kbTn.jpg)

In the case that multiple categories match your search terms, the dropdown above the search box will allow you to select from
one of them.

![Category Search Multiple](https://imgur.com/PFkNn2r.jpg)

### Assignee Search
Similarly to categories, since Northwestern has somewhere in the area of 150 assignment groups (in this workspace alone),
this extension provides a search box for assignees. The search enables you to search for any of these fields:
* An individual's NetID
* An individual's name
* An assignment group's name

For example, to find **NUIT-TSS-USSTier2**, you could search for "sst" (since that's in the name), "kbb0737" (a member's NetID),
or "barnick" (part of a member's name).

![Assignee Search by Team Name](https://imgur.com/Txh81Ji.jpg)

![Assignee Search by Member Name](https://imgur.com/lahPuZG.jpg)

![Assignee Search by Member NetID](https://imgur.com/wavaW6E.jpg)

### Template Search
To make finding a Quick Issue Template easier, the extension adds a search bar to the left of the template menu. The template list will be
filtered to show only templates whose names contain the entered text (case-insensitive).

![Template Search](https://imgur.com/XfrBSV2.jpg)

### Tabbed Browsing Changes
Generally, because of the way that Footprints was written, tickets end up opening in new windows the majority of the time,
regardless of whether your browser is configured to prefer new tabs or new windows. This extension changes that and makes it
such that tickets open *in new tabs* in most places. This behavior can be disabled in the [extension settings](chrome://extensions/?options=bhcajiiignledggebpaalkpcccbjohhc).

### Address Book Search Glitch Fixes
Because of the way that the Footprints address book form was designed, when pressing "Enter" or "Return" to auto-fill contact
information for a ticket, this sometimes caused the last description for a ticket to open in a new window. This extension resolves
that issue.

### Attachment Preview
To view images that are attached to Footprints tickets, Footprints requires that they be downloaded to your computer and then viewed
using a photo viewer on your desktop.

This extension allows for image attachments (`.png`, `.gif`, `.bmp`, and `.jpg`) and text attachments (`.csv`, `.txt`, and `.json`) to be previewed when hovering over the **Download** button for said attachment.

 ![Image Attachment Preview](https://imgur.com/4AmptLN.jpg)

 ![Text Attachment Preview](https://imgur.com/0QcwTuM.jpg)

### Fixify Descriptions
The Footprints WYSIWYG editor has plenty of glitches in its behavior. Often, a description that looked good while typing appears different
after being submitted and results in tickets that have strange discrepancies in formatting, like this one:

![Poorly Formatted Ticket](https://imgur.com/ujxhjEj.jpg)

This extension adds what we lovingly call the **Fixify** button to the description editor. When you click the Fixify button, the following
happens to your ticket description:
* All background highlight colors are removed from the text.
* The text is all set to 13px (10pt) Verdana.
* The color of all text in the ticket is set to black (except for links).

Of note, **bolded**, *italicized*, or indented text will remain bolded, italicized, or indented. All of the above changes will still be made.

![Fixify](https://imgur.com/xlVx6DD.jpg)

Even when it appears that the formatting of a new ticket description is okay, we recommend using the Fixify button to ensure that all redundant
and unnecessary formatting is cleared from the text before submitting. Often, the offending formatting tags are already in the text but don't
cause an issue until the email has already been sent to the user. Fixify prevents that.

### Jump to Ticket Shortcuts
This extension adds a few shortcuts to jump to tickets quickly. From anywhere within the browser, you can do one of three things to jump directly
to a specific ticket:
* Enter the ticket number in the extension menu.
* Highlight the ticket number in text and select "Jump to ticket" from the context menu.
* Type "FP [ticket number]" in Chrome's Omnibox.

### CONDUITS Work Order Contact Display Changes
This extension greys out the names of Feinberg IT contacts in the list of CONDUITS Work Order Contacts since these names are rarely relevant and
should not be given to the users as valid work order contacts. This setting can be disabled in the options.

### Extension Menu
Simply click on the extension menu in the top right, enter the ticket number in the "Jump to ticket" box, and select "Go".

![Extension Menu Jump](https://imgur.com/9H1T0Nr.jpg)

### Context Menu
Highlight a ticket number in text anywhere in the browser, right click to show the context menu, and select "Jump to ticket".

![Context Menu Jump](https://imgur.com/Xs9QRvS.jpg)

### Omnibox
Go to Chrome's Omnibox, clear the contents, and then type "FP [ticket number]" (e.g. "FP 839901") and press "Return" or "Enter".

![Omnibox Jump](https://imgur.com/e6kq1X5.jpg)

## Installation
The extension can be installed in Google Chrome on the Chrome Web Store
[here](https://chrome.google.com/webstore/detail/footprints-selector/bhcajiiignledggebpaalkpcccbjohhc).

## Acknowledgements
Thank you to [@tuchandra](https://github.com/tuchandra) for the original idea to create a Chrome Extension for Footprints.
