# Communication

## Purposes

Our communication process has to serve the following purposes.

| #  | Purpose                 | Example                                                                                                                                                                  | Update Frequency                 | Validity                     |
|:---|:------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------|:-----------------------------|
| 1  | 🚨 Alerting            | THE SERVERS ARE ON FIRE!                                                                                                                                                 | Hopefully every couple of months | 10 minutes                   |
| 2  | 🔀 Ad-Hoc Coordination | "Where can I find this library you told me about?""Who's coming for lunch?""I'll work from home tomorrow."                                                               | Hourly                           | 1-2 hours                    |
| 3  | 👋 Notifications       | RTS Deux from yesterday was sent out just now.                                                                                                                           | Hourly                           | 1-2 hours                    |
| 4  | 🛠 Code Reviews        | I implemented an automatic recovery mechanism for when a stream fails.                                                                                                   | Daily                            | 2-3 days                     |
| 5  | 🎟 Issue tracking      | SRG wants to send us protocols through smoke signals. We need to build a new airflow operator.                                                                           | Daily                            | 3 to 6 weeks (one cycle)     |
| 6  | 🔭 Planning            | "In the next cycle we should tackle monitoring because I want to get some sleep.""Let’s discuss how we want to split this project into front- and backend."              | Weekly                           | A week or for the next cycle |
| 7  | 📝 Documentation       | "This is how we onboard new colleagues.""This is our cluster setup and what you need to do if a node crashes."                                                           | At least once per cycle          | Until updated                |
| 8  | 💡Knowledge Sharing    | In the last cycle we used this new feature engineering library and the pros and cons are the following:                                                                  | At least every cool-down         | 2-3 months                   |
| 9  | 👀 Retrospectives      | In the last cycle we finished the Rio prototype. We struggled with... But this worked fine ...                                                                           | Every cool-down                  | 2-3 months                   |
| 10 | 😍 Team building       | I found this Karaoke Bar where they only play 80s songs, who's in?                                                                                                       | Every couple of months           | 2-3 months                   |
| 11 | 🗣 Feedback            | I like how you comment your code, and you did a great job at setting up the alerting system. I feel you could improve by making your pull requests easier to understand. | Every quarter                    | 3 months                     |

## Different tools for different purposes

### 🚨 Alerting            

For critical alerts, we use **automated phone calls**. Since smartphones
can be set to silent and still ring for specific numbers, this allows us
to unwind, knowing that we will hear our phone if something critical
needs our attention.

### 🔀 Ad-Hoc Coordination                                            

For ad-hoc coordination, we use **Slack**. Since real-time chat, and
especially the notifications, can be disruptive to productivity, we only
use it for messages that have a short lifetime. Everything else should
be handled in code reviews, issues, a GitHub Gist or `.md` files.

We do not require people to be online on Slack. If you are online, you
should be in the "Do Not Disturb" mode most of the time. If we need
somebody's attention urgently, we walk over to that person or give them
a phone call on WhatsApp.

See below the list of channels that we start with. Channels that
everybody should subscribe to are in **bold**. This list can be extended
if necessary, but especially the list of channels that require everybody
to be subscribed should be kept short.

#### Notification channels:

- **`#admin`**: emails to admin@genistat.ch
- `#protocol-export-email`: emails to sendeprotokolle-export@genistat.ch
- `#sendeprotokolle-email`: emails to sendeprotokolle@genistat.ch

#### Alerting channels:

- **`#airflow-alerts`**: notification from failing DAGs
- **`#alerts-dev`**: non production alerts
- **`#rancher-alerts-production`**: notifications from Rancher

#### Ad-hoc/random communication channels:

- **`#general`**: general questions like "who's coming to the office
  today?"
- **`#standup`**: daily standup messages

- `#metadata-managers`: general discussions with metadata managers
- `#segmentation-daily`: daily communication channel for segmentation
  work
- `#segmentation-updates`: announcements regarding sports segmentation
- `#samasource-genistat`: communication with Samasource

- `#music`: any music recommendations
- `#random`: funny, stupid, non-work related things


### 👋 Notifications                                               

For everything on GitHub, we use the GitHub notifications. They can be
selectively silenced or turned on for repositories and issues. We are
expected to check in on the GitHub notifications at least every 24h. If
you are asked for feedback and can't provide it within 24h, say so, to
unblock the colleague asking.

For some notifications that aren't GitHub, we use Slack channels (see
`Notification Channels` above).

### 🛠 Code Reviews       

Because we see pull requests as an excellent way to share knowledge, we
require all the code to go through a PR. To make sure that we can still
move fast where needed, we do two things:

1. We review PRs quickly and treat it as a high priority job. PRs should
   be reviewed within **24h** during the week. If you can't make it, say
   so and potentially assign somebody else.
2. We adapt to the context of the PR. A prototype does not need to cover
   all edge cases, the PRs can be larger and the reviewer does not need
   to scrutinise every detail. Code should always be understandable
   though.

### 🎟 Issue tracking 

We use GitHub issues to track and discuss issues. We use labels to
assign issues to the cycle project that we are working on. Create labels
with the following format: `C{cycle_number}: {project_abbreviation}`. A
label for the Politician Map project in cycle one would have been `C1:
PM`.

Following ShapeUp, we also use labels to assign issues to
[scopes](https://basecamp.com/shapeup/3.3-chapter-11).

### 🔭 Planning                                                  

To plan we use GitHub Issues with the `💡 Pitch` or `🗣 Discussion`
label in the Genistat HQ project.

If we want a face-to-face discussion, we do so and document the results
at a later time.

### 📝 Documentation                               

We document our code as `.md` files in the `/docs` folder in the
respective GitHub repo. We use `README.md` as the index page that links
to the documentation.

Documentation also goes through PRs and should be checked for clarity
and correctness.

Ideally, we write the documentation together with the code.

### 💡Knowledge Sharing                                                                                                                                                                                                                                                                            

We have different types of knowledge that we want to share.

We use GitHub Issues for knowledge that we want to share internally. We
use the following labels:

*  `📣 Announcement` for when things change , r we took an important
   decision.
*  `✨fyi` for information that does not warrant an announcement but
   some might still find useful.
*  `😎 Cool stuff` for cool libraries or articles that you want to
   share with the team.
*  `❤️ Heartbeat` when you want to give an update on how things are
   going

Sometimes, we might want to share knowledge that is not documentation
but is supposed to have a longer lifespan than a GitHub issue. This
includes blog posts or this handbook. For this type of content, we write
`.md` files that go through a PR.

*This section will be updated, once we had our first tech-talk.*
Everybody is free to organise a tech-talk. Those should ideally take
place within the cool-down. Tech-talks should be archived by putting the
slides where they can be found later: A `.md` file pointing to all of
the past tech-talks might be a pragmatic solution. Ideally, we also
record the tech-talk for later viewing by colleagues who couldn't attend
or join Genistat later.

### 👀 Retrospective                        

Retrospectives happen every cool-down. We write one retrospective for
each cycle project. We post them as a GitHub Issue with the `👀
Retrospective` label.

A retrospective should contain a section that describes what went well
and what didn't. Those learnings inform our work in the next cycle,
continuously improving the quality of our work.

### 😍 Team building                                                        

Spending quality time together is essential to us. This includes short
events like dinners and going to the movies together. However, we also
plan on doing more extended activities, where we travel somewhere
together and work remotely. Discussions for social events happen as
GitHub Issues with the `😍 Team building` label.

### 🗣 Feedback     

*This section will be updated once we had our first performance review.*
Feedback is important to us. Knowing where we stand gives us clarity on
what can be improved. We run period performance reviews based on peer
feedback every three months. The primary tool are questionnaires, where
we rate the work of our colleagues as well as our own.
