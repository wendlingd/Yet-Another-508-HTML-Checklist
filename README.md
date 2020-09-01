> :warning: **Source guidelines have changed**: https://www.hhs.gov/web/section-508/accessibility-checklists/index.html, Web Site checklist, will need to be analyzed to see how this project should be changed.

# Yet-Another-508-HTML-Checklist
Section 508 procedures and remediation advice in one interactive page

## Design challenge ##

1. Support accessibility testers AND the authors who are submitting work, through a self-service testing resource used by the organization gatekeepers and subject matter experts/the content authors; show BOTH sides of the work - the test procedures AND the remediation advice; testers can send "Just-In-Time" SPECIFIC advice to the author as the files are turned back for more work
2. Multiple testers should operate from the same enforced "floor" of testing procedures, to be consistent across the enterprise; if one inaccessible file is tested by five testers, the same, correct diagnosis should be given, and the same, correct remediation advice should be given, by all five
3. Tell the web content author exactly what the first ~2 problems are, and then tell them to run this checklist themselves before re-submitting
4. Order procedures to FIRST cover the most common errors by the content authors/novice testers (the organization's subject matter experts); other staff, being more familiar with accessibility, will rely on this tool less
5. Don't use a database. This Minimum Viable Product (MVP) does not use a database so the checklist can be used as one page on an intranet or even one page loaded into the browser from disk - interactivity without back-end complexity; anyone can run it within minutes, with minimal set-up. But, lack of server-side processing means that this file must support sufficient client-side accessibility.

## Long-term impacts (we hope) ##
1. The enterprise enforces the low end of accessibility requirements consistently across multiple testers and across the enterprise
2. Novice testers SOLVE THEIR PROBLEMS today and get their content posted; they do not try to boil the ocean under deadline pressure; they don't need to learn everything immediately. They can focus on what is WRONG, NOW and still meet their publishing deadlines
3. Novice testers BUILD THEIR SKILLS over time in concrete ways, by learning as they publish
4. While the enterprise has churn among authors, new authors are not confused (or not for very long) about what is required of them
5. Allow authors to test themselves to the enterprise standard before content submission or re-submission
6. Save time for the testing group by sending the author to authoritative resources to solve their problems.

## View the checklist ##

BUT some networks block the interactivity code, so if the remediation advice does not appear when you check a box, you may need to run the code locally in order to work...
http://htmlpreview.github.com/?https://github.com/wendlingd/Yet-Another-508-HTML-Checklist/blob/master/HTML-checklist.html

## Problems ##

The interactivity comes from a JavaScript self-posting form. When a checkbox is checked, remediation advice is written into the textarea id="emailText". Shouldn't the user be notified of the new remediation advice that has appeared on the screen? Part of the page has been updated. How might a person hear from the screen reader what the new content is? NVDA just says, "Check." I think the entire remediation block should be read when a box is checked, and if the checkbox is clicked to remove remediation advice, there should be a different message read. But, I'm out of my depth; perhaps there's a better solution?

I would not want to promote an accessibility testing tool that is not itself accessible.

### Primary JavaScript accessibility issue with this checklist (I assume) ##

How to announce remediation advice at the onclick event (click or spacebar - this is a device-independent event handler), WITHOUT moving the keyboard focus from the current procedure.

### Perhaps relevant ###

- https://www.w3.org/WAI/WCAG21/Understanding/name-role-value (WCAG21 4.1.2)
- https://www.w3.org/WAI/WCAG21/Understanding/status-messages.html (WCAG21 4.1.3)
- https://www.w3.org/WAI/WCAG21/Understanding/focus-order (WCAG21 2.4.3)
- https://www.w3.org/TR/wai-aria-practices-1.1/#checkbox (WAI-ARIA Authoring Practices 1.1)

