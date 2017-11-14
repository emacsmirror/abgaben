abgaben.el (German for what students return when given assignments)
is a set of functions for dealing with assignments.  It assumes
that you use mu4e for your mails.

The basic worklfow is as follows:
You receive mails with assignments from your students
You use an attachment action where you
 - select the group this assignment belongs to
   e.g. you have several different courses or (as I usually have)
   two groups for your practical
 - select the current week

![save an assignment](http://arne.chark.eu/2017/11/13/abgaben/save-abgabe-crop.webm)

It then saves that attachment to ABGABEN-ROOT-FOLDER/[group]/[week]/
and creates the directories as needed.
After that, it produces a new heading in your ABGABEN-ORG-File
under ABGABEN-HEADING / [group] / [week]
containing a link to the saved attachment and the email.
(Note: The ABGABEN-HEADING / [group] heading needs to exist already,
	   the week heading will be created if it does not exist)

You can then open the PDFs from your org file and annotate them.
After your annotations, you can use
abgaben-export-pdf-annot-to-org to export your annotations as
subheadings of the current assignment.  This export will capture
all points you have given by matching your annotation lines to
abgaben-points-re and summing the points achieved and achievable
points.

![annotate pdf](http://arne.chark.eu/2017/11/13/abgaben/annotate-pdf-crop.webm)

You can then invoke abgaben-prepare-reply to open the original
mail.  You will have a reply in your kill-ring prepared with your
annotations exported as text and the annotated pdf as attachment.

Press reply, yank, send, your are done!

![send the email](http://arne.chark.eu/2017/11/13/abgaben/send-email-crop.webm)


There is also [a slightly longer explanation](http://arne.chark.eu/2017/11/13/abgaben/) at my blog.
