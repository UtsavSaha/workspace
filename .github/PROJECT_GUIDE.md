# AWS Solutions Architect Learning Path - GitHub Project Guide

## 🚀 Quick Start

This GitHub repository is set up to track your 12-week AWS Solutions Architect Associate certification journey. Here's how to get the most out of it:

## 📱 Setting Up GitHub Notifications

### Enable Email Notifications:
1. Go to **Settings** → **Notifications** (top right corner)
2. Under "Email notification preferences":
   - ✅ **Participating**: Get notified when you're involved
   - ✅ **@mentions**: Get notified when mentioned
   - ✅ **Custom**: Set up custom notification rules for this repo
3. Choose your preferred frequency:
   - Real-time (instant)
   - Daily digest
   - Weekly digest

### Set Custom Rules for This Repository:
1. In Notifications Settings, click **Custom**
2. Add rule for this repository:
   - **Repository:** aws-learning-path
   - **Notifications:** Participating and @mentions
   - **Check:** Issues, Pull Requests, Releases

## 📋 Using Issues for Daily Tracking

### Creating Daily Study Issues:
1. Go to **Issues** tab
2. Click **New Issue**
3. Select **Daily Study Task** template
4. Fill in:
   - Date (YYYY-MM-DD format)
   - Topic name
   - Learning objectives
5. Add relevant labels:
   - Pick one: `daily-task`
   - Add topic: `topic-ec2`, `topic-s3`, etc.
   - Priority: `priority-high`, `priority-medium`, etc.
6. **Assign to yourself**
7. Click **Create**

### Updating Daily Issues:
- Check off items as you complete them
- Add comments with key learnings
- Update "Self-Assessment" section
- Close when complete

### Tips:
- Create issues at the start of each week for the whole week
- Or create the night before for the next day
- Use issue comments to store quick notes
- Reference with `#issue-number` in other issues

## 📊 Using Milestones for Weekly Tracking

### Creating Weekly Milestones:
1. Go to **Issues** → **Milestones** (top right)
2. Click **New Milestone**
3. Title: `Week [N] - [Topic Name]`
4. Due date: End date of that week
5. Description: Main objectives for the week
6. Click **Create Milestone**

### Linking Issues to Milestones:
1. Open a daily issue
2. On the right panel, click **Milestone**
3. Select the appropriate week's milestone
4. All daily issues for that week should be linked

### Viewing Progress:
- See percentage completion for each milestone
- Milestones show which weeks are complete, on track, or behind

## 🏷️ Using Labels for Organization

### Recommended Label Strategy:

**For Daily Tasks:**
```
Labels: daily-task, topic-[service], priority-[level], status-[status]
Example: daily-task, topic-ec2, priority-high, status-pending
```

**For Weak Areas:**
```
Labels: priority-high, needs-review, topic-[service]
Example: priority-high, needs-review, topic-networking
```

**For Hands-On Labs:**
```
Labels: hands-on-lab, topic-[service], status-in-progress
Example: hands-on-lab, topic-ec2, status-in-progress
```

### Filter Issues by Label:
- Click any label to filter
- Combine multiple labels for focused view
- Use GitHub search: `label:priority-high label:topic-ec2`

## 📅 Scheduling & Reminders

### GitHub Actions for Automated Reminders:
This project includes automated workflows:
- ✅ **Daily Reminder** - 9 AM UTC each day (customizable)
- ✅ **Weekly Summary** - Sunday 6 PM UTC (customizable)

### Customizing Reminder Times:
1. Go to **Settings** → **Actions** → **General**
2. Edit `.github/workflows/daily-reminder.yml`
3. Modify the `cron` schedule:
   - Format: `'minute hour * * weekday'`
   - Example: `'0 8 * * 1-5'` = 8 AM weekdays only
   - [Cron Reference](https://crontab.guru/)

### Third-Party Calendar Integration:
- Export your milestones to Google Calendar
- Set custom reminders in your phone calendar for study time
- Use tools like IFTTT to integrate GitHub issues with reminders

## 📈 Tracking Progress

### Daily Progress:
1. Check notifications for daily reminders
2. Open that day's issue
3. Update status as you complete sections
4. Close when day is done

### Weekly Review:
1. Sunday issue will auto-create with weekly summary
2. Review all 7 daily issues from the week
3. Calculate average score if you took a quiz
4. Update milestone with completion percentage
5. Note weak areas for future focus

### Monthly Progress:
1. Review first week of each 3-week period
2. Check if on track vs. behind/ahead
3. Adjust study time if needed
4. Celebrate milestones!

## 🎯 Example Workflow

### Monday - Start of Week:
1. Open GitHub Issues
2. See weekly reminder from Sunday
3. Create daily issues for Monday-Sunday (or just today)
4. Link all to this week's milestone
5. Start with Monday's issue

### Daily (Weekday):
1. Get notification from GitHub reminder
2. Open today's issue
3. Study for 30-60 minutes
4. Check off completed sections
5. Add learning notes in comments
6. Close issue at end of day

### Sunday - End of Week:
1. Finish all 7 days of issues
2. Create or update weekly milestone summary
3. Score this week's quiz
4. Review failed questions
5. Document weak topics
6. Get ready for next week

### Every 3 Weeks:
1. Review overall progress
2. Adjust study pace if needed
3. Focus on weak areas from quizzes

## 🔔 Important Settings to Configure

### Repository Watch Settings:
1. Click **Watch** (top right)
2. Select:
   - **Watching** for all updates
   - **Custom** to be selective

### Issue Notification Rules:
1. **Settings** → **Notifications**
2. Create custom rule:
   - Check `Issues`
   - Uncheck `Discussions` (if not used)
   - Set frequency to your preference

## 💡 Pro Tips

1. **Templates Matter:** Use the provided issue templates to stay organized
2. **Consistent Labeling:** Always use the same labels for easy filtering
3. **Comments for Notes:** Use issue comments to store study notes instead of creating separate docs
4. **Milestones for Roadmap:** Milestones show your overall progress
5. **Close Done Issues:** Closing issues gives visual progress
6. **Export Data:** GitHub provides CSV export of issues for tracking
7. **Search Power:** Use GitHub's advanced search to find specific topics
8. **Project Board:** For visual kanban-style tracking, create a GitHub Project Board

## 🎓 When You Pass the Exam

1. Create final issue: "✅ AWS Certification Exam - PASSED"
2. Add your score and date
3. Lock discussions
4. Star the repository as a learning accomplishment
5. Consider sharing your journey with others!

---

**Questions?** Refer back to individual templates or GitHub's help documentation.

**Let's get certified! 🚀**
