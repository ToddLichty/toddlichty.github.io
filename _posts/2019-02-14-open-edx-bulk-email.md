---
layout: post
title: Open edX - Bulk Email
permalink: /open-edx-bulk-email/
author: Todd Lichty
---
<p>One of the items I need to investigate with regards to Open edX is the bulk emailing functionality it offers. There is an enormous amount of research that indicates that weekly updates/announcements from staff have a significant effect on whether students will complete an online course. This makes the bulk email feature a must have on any LMS platform we choose.</p><p>To send an email to all learners in the course, you must login to the LMS with the instructor's email. Once on the course home page, you will see the <em>Instructor</em> menu item appear in the top menu:</p><figure class="kg-card kg-image-card"><img src="/images/course_dashboard.png" class="kg-image"></figure><p>Clicking on this menu item will initially load the <em>Instructor Dashboard</em> for the the course:</p><figure class="kg-card kg-image-card"><img src="/images/dashboard_original.png" class="kg-image"></figure><p>Notice the lack of an "Email" menu item. To fix this, you need to login to the Django admin of the LMS and add a Bulk_Email flag value. From the Django admin home page, scroll down to the <a href="http://localhost:18000/admin/bulk_email/"><em>BULK_EMAIL</em></a> section:</p><figure class="kg-card kg-image-card"><img src="/images/bulk_email_flag_menu.png" class="kg-image"></figure><p>Click the Add link beside Bulk email flags and check off the checkbox beside Enabled. Click the Save button.</p><figure class="kg-card kg-image-card"><img src="/images/bulk_email_flag.png" class="kg-image"></figure><p>I restarted the LMS container just to be sure and then went back to the I<em>nstructor Dashboard</em> and the Email menu item was then showing:</p><figure class="kg-card kg-image-card"><img src="/images/instructor_dashboard_email.png" class="kg-image"></figure>