# Yet-Another-508-HTML-Checklist
Section 508 procedures and remediation advice in one interactive page

## Design challenge ##

1. Support accessibility testers AND authors who are submitting work
2. Multiple testers should use the same "floor" of testing procedures, to be consistent across the enterprise
3. Tell the web content author exactly what the first ~2 problems are, and then tell them to run this checklist themselves before re-submitting
4. Implement BOTH the test procedures AND remediation advice; send the "Just-in-time" advice to the author as you turn the file(s) back for more work - within the CMS or in email
5. Don't use a database. By not using a database the checklist can be used as one page on an intranet or even one page loaded into the browser from disk - interactivity without a complex back end.

## Long-term impacts (we hope) ##
1. Novice testers solve their problems today and get their content posted
2. Novice testers get better over time in concrete ways, by learning as they publish
3. Novice testers do not try to boil the ocean when trying to get content publishedl; they don't need to learn everything immediately. They can focus on what is WRONG, NOW
4. The enterprise enforces the low end of accessibility requirements consistently across multiple testers and across the enterprise
5. While the enterprise has churn among authors, new authors are not confused (or not for very long) about what is required
6. Web authors gain knowledge and skills over time, even under deadline pressure
7. Allow authors to test themselves to the enterprise standard
8. Save time for the testing group by sending the author to authoritative resources.

## View the checklist ##

BUT the interactivity will not work in this Preview mode...
http://htmlpreview.github.com/?https://github.com/wendlingd/Yet-Another-508-HTML-Checklist/blob/master/HTML-checklist.html

## Problems ##

The interactivity comes from a JavaScript self-posting form. When a checkbox is checked, remediation advice is writeen into the textarea id="emailText". Should the user be notified of this new remediation advice. Part of the page has been updated. How might a person hear from the screenreader, what the new content is? NVDA just says, "check." I think the entire remediation block should be read? But, I'm out of my depth; perhaps there's a better solution?

I would not want to promote an accessibility testing tool that is not itself accessible.
