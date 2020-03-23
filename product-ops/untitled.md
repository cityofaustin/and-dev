# Github and Zenhub Basics

The Data and Technology Services team is using [Github](https://github.com/) and [ZenHub](https://www.zenhub.com/) for agile project management.

## Set up

1. [Create a Github account](https://github.com/join) if you don't have one already.
2. Have someone on the DTS team add you to the [City of Austin](https://github.com/cityofaustin) organization and the [Transportation](https://github.com/orgs/cityofaustin/teams/transportation) team as a Maintainer.
3. Add the [ZenHub extension](https://www.zenhub.com/extension) to your browser.

## Repos \[needs to be updated\]

We organize our work into repositories. In a given repository:

* The root directory stores version-controlled application code and assets
* The wiki contains documentation for end users and/or developers
* Issues are used to manage feature requests, bug reports, and all the work the project involves — stakeholder meetings, user research, testing,

Most applications have their own repo, but there are three repos that we use to manage multiple projects and tasks:

* [**atd-data-tech**](https://github.com/cityofaustin/atd-data-tech) — General DTS operations
* [**atd-amanda**](https://github.com/cityofaustin/atd-amanda) — Projects built on the [Amanda](https://github.com/cityofaustin/atd-amanda/wiki) platform
* [**atd-geospatial**](https://github.com/cityofaustin/atd-geospatial) — GIS and geodata projects

You can see a full list of our repos [here](https://github.com/orgs/cityofaustin/teams/transportation/repositories) and instructions for setting up new repositories here.

## Issues

Tracking our work in issues not only helps us stay organized, it gives us data on where we're spending our time. To create an issue, click the green "New issue" button in the upper right on the _Issues_ page or our [Zenhub board](https://github.com/cityofaustin/atd-data-tech/blob/master/.github/settings.yml#workspaces/data--tech-services-5caf7dc6ecad11531cc418ef/board).

![Screenshot of the Issues page with the &quot;New issue&quot; button circled. ](https://github.com/cityofaustin/atd-data-tech/raw/master/images/Create-new-issue.png?raw=true)

## Labels

You can apply labels when you're looking at an individual issue by clicking the "Labels" link on the righthand side. You can also add labels in bulk from the __[_Issues_ page](https://github.com/cityofaustin/atd-data-tech/issues) or [our ZenHub board](https://github.com/cityofaustin/atd-data-tech#workspaces/data--tech-services-5caf7dc6ecad11531cc418ef/board). 

Labels are critical for filtering on the Zenhub board, so **it's important to make sure every new issue has**:

* _**Workgroup**_ — the customer we're serving; _**Workgroup: DTS**_ for internal work and _**Workgroup: ATD**_ for department-wide work
* _**Service**_ — The service team the work will be handled by
* _**Project**_ **** and/or _**Product**_ labels
  * _**Projects**_ refer to a substantial scope of related work that will reach a state of relative completion, such as the [AGOL Audit](https://github.com/cityofaustin/atd-data-tech/issues/253) 
  * _**Products**_ are solutions that we continue to support over time, including all in-house applications, such as the Vision Zero Crash Data System
  * Often, a major feature or enhancement to an existing product will require enough resources and coordination that it qualifies as a project. [Warehouse Inventory](https://github.com/cityofaustin/atd-data-tech/issues/20), for example, was a major set of features and enhancements to the Finance and Inventory App, so needed both ****_**Product**_ ****and ****_**Project**_ ****labels 
  * Some issues, such as [this](https://github.com/cityofaustin/atd-data-tech/issues/1010), don't need either a _**Product**_ or _**Project**_ label. But most do! 
* _**Type**_ — The type of request or task 

Optionally, these are very useful:

* _**Impact**_ or _**Need**_ — to designate priority; _Need_ referring to features or enhancements while _Impact_ applies more to bugs

If you find yourself making issues with the same labels over and over while you work on a project, you can create an issue template to use. \(need to explain\)

## Estimates

Estimates are how we track the level of effort of issues. This is useful for

* Sprint planning to see when a person or team has too many issues \(or too few!\) issues assigned to them
* Stakeholder discussions when prioritizing features — being able to show stakeholders easily that we can accomplish, say, three small tasks, two medium, or one large
* [Velocity tracking](https://www.zenhub.com/blog/track-your-speed-of-work-with-agile-velocity-charts/), which helps us predict the likelihood we can complete things by a given date

[This is a good article](https://help.zenhub.com/support/solutions/articles/43000010347-estimate-work-using-story-points) about the hows and whys of estimates with ZenHub.

![Estimates \(1-5\) align with shirt sizes \(XS-XXL\). Complexity, uncertainty, and time increase as numbers/sizes increase](https://github.com/cityofaustin/atd-data-tech/raw/master/images/Relative-estimates.png)

## Epics

Epics are a powerful feature that ZenHub adds to Github. They allow you to group related tasks together and easily track them from one place. [Here is a solid guide to how they work](https://www.zenhub.com/blog/working-with-epics-in-github/). And [here is an example](https://github.com/cityofaustin/techstack/issues/1215) from another City of Austin project.

For tasks that are ongoing such as a recurring meeting, it may help to create an epic and put the individual instances of the tasks inside it. [Here is an example](https://github.com/cityofaustin/atd-geospatial/issues/4) of that type of usage for a task performed for a customer on a regular basis.

Epics do not need estimates assigned to them manually. Instead, the effort is represented by the total of all the story points in the issues the epic contains.

In the end, epics can be used to group whatever makes sense for you and your collaborators. Some people prefer [issues with task lists inside them](https://github.com/cityofaustin/techstack/issues/616). That's fine as long as the issue doesn't end up needing more effort than we can represent in our [estimate scale](https://github.com/cityofaustin/atd-data-tech/wiki/Project-Management:-Github-and-ZenHub-Basics#estimates) for a single issue.

## Pipelines

The Zenhub board uses a [Kanban](https://en.wikipedia.org/wiki/Kanban_board)-like format where issues are represented as cards and move across the board as they enter various stages of completion. Our workspace pipelines are:

* _**New Issues**_ - Awaiting triage by a product manager.\*
* _**Icebox**_ - Recorded and understood, but not committed to. Lack evidence of overall value or applicability. We don't want to delete these and create a cycle of raising duplicate issues, so we keep them in our icebox with just enough information attached that we can pick it up some time in the future — if and when we choose to do so.
* _**Needs Scoping**_ - Potential projects that require clarification or exploration. Gathering the information we will need to prioritize and assign these projects moving forward might entail a phone call, an email, or a discovery meeting.
* _**Backlog**_ - Defined issues that are ready to be tackled by the team when the time comes. This pipeline is prioritized: the higher an issue is on this list, the higher the priority. Higher-priority items will typically have more in-depth information attached.
* _**On Deck**_ - Slated for work in the current sprint. During Sprint Planning, we pull all issues that we intend to work on during the sprint into _On Deck_.
* _**In Progress**_ - This one is self-explanatory. ;\) Each Issue in this pipeline should have an assigned owner who is responsible for its completion.
* _**Blocked** -_ Issues that we intend to complete in the current sprint but have unmet dependencies — often awaiting CTM support or user feedback.
* _**Recurring**_ - 
* _**Review/QA**_ - Proposed as complete but awaiting approval before closure. Approval takes various forms depending on issue type. For issues connected to code requests, this might be a code review. For feature implementations, this may be acceptance testing.
* _**Ready to Deploy**_ - Code or configuration that is ready to be deployed to production. 
* _**Closed**_ - Done! 🙌

_\*When you create new issues that do not need need PM eyes, make sure to promptly move them into the appropriate pipeline._

## Assignees

An issue should be assigned to the person/people who will tackle it. This is important as it allows everyone to easily filter down to issues they are responsible for.

### Bulk editing issues

_TO DO: Explain how to do stuff from the Issues page or_ [_our ZenHub board_](https://github.com/cityofaustin/atd-data-tech#workspaces/data--tech-services-5caf7dc6ecad11531cc418ef/board)_._
