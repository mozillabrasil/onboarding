This page is specifically about [https://github.com/mozilla the "mozilla" organization on github]. There are several other github organizations you may be interested in, cf. the incomplete list [[#other_github|below]].
<div id="contact">
{| class="wikitable"
|-
! [[File:Red_question_mark.png|144px|Send us an email!|link=]] Got a question?
|-
| Email {{emailentry|github-owners|mozilla.org|at=is}} <br />
Bugzilla [https://bugzilla.mozilla.org/enter_bug.cgi?comment=I%27ve%20read%20https%3A%2F%2Fwiki.mozilla.org%2FGithub%2C%20and%20need%20help%20with%20the%20following.%0D%0A%0D%0A&component=Github%3A%20Administration&form_name=enter_bug&product=mozilla.org& mozilla.org :: Github: Administration] <br />
irc #github on [[IRC|moznet]]
|}

== News ==
* As of June 20, 2016, all members [https://groups.google.com/forum/#!topic/mozilla.dev.platform/UmHOOh3qtiM must have 2FA enabled]. You have been notified if this impacts you.

== Recommendations and FAQ ==

=== Where should I ask additional questions? ===
* Send an email to '''{{emailentry|github-owners|mozilla.org|at=is}}''' and we'll respond right away! We're also available on #github on irc.

=== How do I hook up a new 3rd party application to a repository in the mozilla org? ===
3rd party applications can easily impact many other repositories than the initial one. For that reason, the following steps are strongly encouraged:
# Create yourself a new github user for this repository.
# Make them an admin of the repository(s) temporarily.
# Sign in as the new github user and setup the 3rd party application.
# Log back into your normal account.
# Try to reduce access of that user from an admin of the repository(s) to read only access.
# If (5) doesn't work, at least the 3rd party application will not have access to all of your normal github account's (including private repositories).

* Authorizing an application to work with GitHub utilizes the permissions your account has -- so, any repositories you have access to the application will have access to as well (including private ones).  If you want to grant access to an application that no one else has used with the Mozilla organization yet you'll see a "Request access" button during the set up flow.  You'll need to click that button to request approval.  See below for an example:

[[File:github_approval.png]]

* In some cases, the application does not need to be "approved" to function correctly, as it has read only access to any public repository. (Some applications only want write access to help you configure the application first time.)

* In other cases, the application does need write permission, and/or permission to read a private repository. In these cases, it is helpful to send the details to the owner's team, either by [https://bugzilla.mozilla.org/enter_bug.cgi?comment=I%27ve%20read%20https%3A%2F%2Fwiki.mozilla.org%2FGithub%2C%20and%20need%20help%20with%20the%20following.%0D%0A%0D%0A&component=Github%3A%20Administration&form_name=enter_bug&product=mozilla.org& opening a bug] or [[#contact|email]].

=== Reviewing owners and permissions ===
As an owner or repository admin you're responsible for maintaining the list of people with access to your projects.  Please be active and prudent about maintaining this list.

=== Can I be an Owner of the Mozilla Organization? ===
The Owners group on github has complete administrative power and will be limited to a minimal number of people and reviewed regularly.  If a person is an owner they are expected to actively participate in the group and assist others as requested.  Owners will be added as a need arises (for example, support in another timezone) as determined by the current owners.

All owners '''must''' have 2FA enabled for their GitHub login. (Everyone else ''should''.)

=== Can I be a Member of the Mozilla Organization? ===
With recent github enhancements (2015), we encourage the following (rough) guidelines, which strongly prefers using github teams. As a reminder, all members of the [https://github.com/mozilla/ Mozilla organization on github] agree to be bound by [https://www.mozilla.org/en-US/about/governance/policies/commit/requirements/ Mozilla's Commit Access Requirements], and should follow the intent of the [https://www.mozilla.org/en-US/about/governance/policies/commit/access-policy/ Mozilla's Commit Access Policy] as much as practical.
* "Outside Collaborator": repository admins can grant outside collaborator to any github account. "Outside Collaborator" is roughly analogous to "Level 1a" access to Mozilla hosted repositories.
* "Team Member": team maintainers can add github users to a team, if they are already a member of the organization. If you are not yet a member of the organization, the team maintainer should [[#contact|request your addition]] to their team, as a form of vouching. "Team Member" is roughly analogous to "Level 2" or "Level 3", with the distinction being the content of the repositories managed by the team.

{{note| As of June 30, 2016, all members of the Mozilla organization on github '''MUST''' have [https://help.github.com/articles/about-two-factor-authentication/ 2FA enabled].|reminder}}

{{note| Automation accounts are also required to have 2FA enabled. Scripts should use [https://help.github.com/articles/creating-an-access-token-for-command-line-use/ access tokens] with minimum permissions to accomplish the task.}}


Some people are interested in being members of the Mozilla organization on github as a way to highlight their contributions to the Mozilla Project. Thanks for your help! And there is a [https://www.mozilla.org/credits/ better place] to highlight your work. Please refer to the [https://www.mozilla.org/credits/FAQ FAQ] for that process.

=== Should I make a separate github organization or just create a repository in an existing one? ===
This is a personal preference.  If you have a large enough project or organization feel free.  We suggest you use the strategies and recommendations here as a model to manage the details.

=== Forking vs Transferring ===
'''Do not "fork" a repository into a Mozilla organization.''' Doing so gives ''every team in the org'' rights to it.

If you have created a repo on your own account (for example, myuser/myrepo) and it should live under the Mozilla organization, here are the steps:

{{note|As soon as you transfer, your repository will be in "limbo" (only you will have write access) until you get the assistance of an [[#contact|org admin]] who can make the changes. Please plan in advance if timing is critical.}}

# If you're not a member of any team, talk to an [[#contact|org admin]].
# Under the repo admin, transfer ownership to the Mozilla organization. If you don't see this option, return to step 1.
# Choose which teams should be given access. All chosen teams will have only 'read' access at this point.
# Ask an [[#contact|org admin]] to grant team permissions higher than read ('write' and 'admin' are the other choices). (Team maintainers do not have the ability to change a repositories status.)
# Fork the repo from Mozilla (mozilla/myrepo) back to your account (recreating myuser/myrepo). While the transferred repo becomes the root of the network on Github (e.g. all forks are now forks of mozilla/myrepo) other users may be pointing to your repo by URL. (Optional, github will redirect old URLs for transfers, but you probably want a local repo if you use the PR workflow.)

=== Do I need to be an owner to create repositories? ===
No.  If a person has read/write access to another repository in that organization they can make more repositories in that organization. However, it's preferred that you create repositories in the context of a team.

=== Are there requirements for when or how I should create a new team? ===
No.  When requirements were proposed they all seemed too rigid and time consuming.  Instead we recommend staying flexible and using good naming and documentation for projects (similar to naming CSS classes or variables).

On large teams we recommend you separate teams for read/write and repository administration.

<div id="other_github"></div>
=== Is "mozilla" the only github "organization" related to Mozilla? ===
No, there are plenty of Mozilla-related "organizations" on github. As a rule of thumb, initiatives that create a large number of sub-repositories will create their own "organization". Here is a (probably incomplete) list of them:
{| class="wikitable sortable"
|-
! Organization !! Description !! Contact Owner
|-
| [https://github.com/mozilla-it mozilla-it] || Mozilla IT's repositories || ?
|-
| [https://github.com/bugzilla bugzilla] || Bugzilla (the product) || #bteam
|- 
| [https://github.com/drumbeat-badge-sprint drumbeat-badge-sprint] || Drumbeat Badge Lab || ?
|-
| [https://github.com/hackasaurus hackasaurus] || Hackasaurus || ?
|-
| [https://github.com/jetpack-labs jetpack-labs] || Jetpack Labs || ?
|-
| [https://github.com/mdn mdn] || Mozilla Developer Network || {{Mozillian|groovecoder|Luke Crouch}}
|-
| [https://github.com/mozbrick mozbrick] || Mozilla Brick (web components library) || ?
|-
| [https://github.com/mozilla-appmaker mozilla-appmaker] || Mozilla Appmaker || ?
|-
| [https://github.com/mozilla-b2g mozilla-b2g] || Mozilla Boot2Gecko / Firefox OS || ?
|-
| [https://github.com/mozilla-bteam mozilla-bteam] || Bugzilla.Mozilla.org || #bteam
|-
| [https://github.com/mozilla-cit mozilla-cit] || Mozilla Community Ops || {{Mozillians|tanner|Tanner Filip}} or {{Mozillians|yalam96|Yousef Alam}}
|-
| [https://github.com/mozilla-comm mozilla-comm] || Calendaring and Messaging related projects || ?
|-
| [https://github.com/mozilla-cordova mozilla-cordova] || Firefox OS Support for Apache Cordova || ?
|-
| [https://github.com/mozilla-metrics mozilla-metrics] || Mozilla Metrics || ?
|-
| [https://github.com/mozilla-raptor mozilla-raptor] || Mozilla Raptor / Firefox OS Performance || {{Mozillian|eliperelman|Eli Perelman}}, {{Mozillian|rwood|Rob Wood}}
|-
| [https://github.com/mozilla-releng mozilla-releng] || Mozilla Release Engineering || #releng
|-
| [https://github.com/mozilla-services mozilla-services] || Mozilla Services || [https://github.com/orgs/mozilla-services/people?utf8=%E2%9C%93&query=role%3Aowner mozilla-services owners]
|-
| [https://github.com/mozilla-svcops mozilla-svcops] || Mozilla Cloud Services Ops || {{Mozillian|relud|Daniel Thornton}}
|-
| [https://github.com/MozillaTW MozillaTW] || Mozilla Taiwan || ?
|-
| [https://github.com/Mozilla-TWQA Mozilla-TWQA] || Mozilla Taiwan QA || ?
|-
| [https://github.com/mozillahispano mozillahispano] || Mozilla Hispano || ?
|-
| [https://github.com/MozillaScience MozillaScience] || Mozilla Science Lab || ?
|-
| [https://github.com/MozillaSecurity MozillaSecurity] || Mozilla Platform Fuzzing Team master repo with many fuzzing tools under it. || ?
|-
| [https://github.com/MozillaWiki MozillaWiki] || MozillaWiki (wiki.mozilla.org) || {{Mozillian|ckoehler|Christie Koehler}}, {{Mozillian|gphemsley|Gordon P. Hemsley}}
|-
| [https://github.com/mozillayvr mozillayvr] || Mozilla Vancouver @MozillaYVR || {{Mozillian|bclark|Brian Clark}}, {{Mozillian|shobson|Stephanie Hobson}}
|-
| [https://github.com/mozfr mozfr] || Mozilla Francophone || Pascal Chevrel https://mozillians.org/fr/u/pascalc/
|-
| [https://github.com/opennews opennews] || Knight-Mozilla OpenNews || ?
|-
| [https://github.com/rust-lang rust-lang] || The Rust Programming Language || {{Mozillian|aturon|Aaron Turon}}
|-
| [https://github.com/servo servo] || Servo (browser engine written in Rust) || {{Mozillian|larsberg|Lars Bergstrom}}, Jack Moffitt
|-
| [https://github.com/tabulapdf tabulapdf] || Tabula project (extract data from PDF files) || ?
|-
| [https://github.com/webcompat webcompat] || Web Compatibility Team || {{Mozillian|miketaylr|Mike Taylor}}
|-
| [https://github.com/mozilla-l10n mozilla-l10n] || Mozilla l10n-drivers team || Pascal Chevrel https://mozillians.org/fr/u/pascalc/
|-
| [https://github.com/taskcluster taskcluster] || [[TaskCluster]] Team || {{Mozillian|sdeckelmann|Selena Deckelmann}}
|-
| [https://github.com/MozillaCH MozillaCH] || Mozilla [[Switzerland]] || {{Mozillian|mkohler|Michael Kohler}}, {{Mozillian|freaktechnik|freaktechnik}}
|}

=== Are there other unofficial or Mozilla-related repositories hosted on Github? ===
Why, yes! In no particular order:

* [https://github.com/kinetiknz/nestegg/ https://github.com/kinetiknz/nestegg/] :  WebM demuxer
* [https://github.com/xiph/opus/ https://github.com/xiph/opus/] :  Modern audio compression for the internet.
* [https://github.com/webmproject/libvpx https://github.com/webmproject/libvpx] :  Mirror only. Please do not send pull requests.
* [https://github.com/campd/fxdt-adapters https://github.com/campd/fxdt-adapters] :  Firefox Developer Tools protocol adapters
* [https://github.com/kripken/emscripten https://github.com/kripken/emscripten] :  Emscripten: An LLVM-to-JavaScript Compiler
* [https://github.com/bbondy/codefirefox https://github.com/bbondy/codefirefox] :  Video and exercise based tutorial site for coding Firefox and other Mozilla related technology
* [https://github.com/nickdesaulniers/where-is-firefox-os https://github.com/nickdesaulniers/where-is-firefox-os] :  A map showing where in the world Firefox OS phones are being sold.
* [https://github.com/jdm/bugsahoy https://github.com/jdm/bugsahoy] :  A landing page to make finding relevant bugs easier for new Mozilla contributors.
* [https://github.com/w3c/web-platform-tests https://github.com/w3c/web-platform-tests] :  Test Suites for Web Platform specifications
* [https://github.com/w3c/wptserve https://github.com/w3c/wptserve] :  Web server designed for use with web-platform-tests
* [https://github.com/w3c/wptrunner https://github.com/w3c/wptrunner] : Cross-browser and multi-platform test runner for web-platform-tests.  Used in mozilla-central and servo.
* [https://github.com/w3c/testharness.js https://github.com/w3c/testharness.js] : (no description)
* [https://github.com/jdm/asknot https://github.com/jdm/asknot] :  Ask not what Mozilla can do for you but what you can do for Mozilla.
* [https://github.com/jeffbryner/MozDef https://github.com/jeffbryner/MozDef]: Mozilla Defense Platform.
* [https://github.com/jgraham/webdriver-rust https://github.com/jgraham/webdriver-rust]: WebDriver library for Rust.
