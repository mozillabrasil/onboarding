Esta página é especifica sobre [https://github.com/mozilla a organização "mozilla" no GitHub]. Existem outras muitas organizações no GitHub que você pode se interessar, cf. a lista incompleta [[#other_github|below]].
<div id="contact">
{| class="wikitable"
|-
! [[File:Red_question_mark.png|144px|Envie-nos um e-mail !|link=]] Dúvida?
|-
| Email {{emailentry|github-owners|mozilla.org|at=is}} <br />
Bugzilla [https://bugzilla.mozilla.org/enter_bug.cgi?comment=I%27ve%20read%20https%3A%2F%2Fwiki.mozilla.org%2FGithub%2C%20and%20need%20help%20with%20the%20following.%0D%0A%0D%0A&component=Github%3A%20Administration&form_name=enter_bug&product=mozilla.org& mozilla.org :: Github: Administração] <br />
irc #github on [[IRC|moznet]]
|}

== Notícias ==
* A partir de 20 de junho de 2016, todos os membros [https://groups.google.com/forum/#!topic/mozilla.dev.platform/UmHOOh3qtiM devem ter habilitado 2FA] Você será notificado se impacta você.

== Recomendações e FAQ ==

=== Onde eu posso realizar mais perguntas? ===
* Envie um email para '''{{emailentry|github-owners|mozilla.org|at=is}}''' e nós responderemos imediatamente! Nós também estamos no canal #github no IRC.

=== Como eu posso enviar um novo aplicativo para um repositório da org. mozilla? ===

3rd party applications can easily impact many other repositories than the initial one. For that reason, the following steps are strongly encouraged:
Desenvolvedoras de aplicativos podem facilmente impactar muitos outros repositórios além do inicial. Por estas razões, os seguintes passos são fortemente encorajados:
# Crie você mesmo um novo usuário no GitHub para este repositório.
# Faça deste usuário o administrador do repositório (ou repositórios) temporariamente.
# Se autentique com o novo usuário do GitHub e configure a aplicação do terceiro.
# Volte e se autentique com seu usuário normal.
# Tente reduzir o acesso daquele usuário administrador do repositório para acesso somente de leitura.
# Se passo (5) não funcionar, pelo menos a aplicação do terceiro não terá acesso as contas de usuários normais (incluindo repositórios privados).

* Autorizar uma aplicação para trabalhar com GitHub utiliza as permissões que sua conte tem -- então, qualquer repositório que você tenha acesso a aplicação também terá acesso (incluindo acesso privado). Se você quer permitir acesso para uma aplicação que ninguém na organização Mozilla tenha utilizado, você verá um botão para "Requisitar acesso" durante o fluxo de configuração. Você precisará clicar naquele botão para requisitar aprovação. Veja abaixo um exemplo:

[[File:github_approval.png]]

* Em alguns casos, a aplicação não necessitará de aprovação para funcionar corretamente, como ela tem acesso de leitura a qualquer repositório público. (Algumas aplicações só querem ter acesso de escrita para ajudá-lo a configurar a aplicação na primeira vez.)

* Em outros casos, a aplicação necessitará de permissão de escrita, e/ou permissão de leitura em repositório privado. Nesses casos, é conveniente enviar os detalhes para o responsável da equipe, seja por [https://bugzilla.mozilla.org/enter_bug.cgi?comment=I%27ve%20read%20https%3A%2F%2Fwiki.mozilla.org%2FGithub%2C%20and%20need%20help%20with%20the%20following.%0D%0A%0D%0A&component=Github%3A%20Administration&form_name=enter_bug&product=mozilla.org& reportando um bug] ou [[#contact|email]].

=== Revisando responsáveis e permissões ===
Como um criador ou um administrador de repositório você é responsável por manter a lista de pessoas com acesso ao seu projeto. Por favor seja ativo e prudente enquanto mantém a lista.

=== Posso ser um responsável da Organização Mozilla? ===
Os responsáveis por grupos no GitHub tem total poder administrativo e serão limitados a um pequeno grupo de pessoas e revisores regularmente. Se uma pessoa é responsável espera-se participação ativa no grupo e suporte aos outros quando requisitado. Outros responsáveis serão adicionados quando surgir a necessidade (por exemplo, suporte em outro fuso horário) conforme determinado pelos atuais responsáveis.

Todos os responsáveis '''deverão''' ter ativo 2FA para suas credenciais no GitHub. (Todo mundo ''deveria''.)

=== Can I be a Member of the Mozilla Organization? ===
With recent GitHub enhancements (2015), we encourage the following (rough) guidelines, which strongly prefers using github teams. As a reminder, all members of the [https://github.com/mozilla/ Mozilla organization on github] agree to be bound by [https://www.mozilla.org/en-US/about/governance/policies/commit/requirements/ Mozilla's Commit Access Requirements], and should follow the intent of the [https://www.mozilla.org/en-US/about/governance/policies/commit/access-policy/ Mozilla's Commit Access Policy] as much as practical.
* "Outside Collaborator": repository admins can grant outside collaborator to any GitHub account. "Outside Collaborator" is roughly analogous to "Level 1a" access to Mozilla hosted repositories.
* "Team Member": team maintainers can add GitHub users to a team, if they are already a member of the organization. If you are not yet a member of the organization, the team maintainer should [[#contact|request your addition]] to their team, as a form of vouching. "Team Member" is roughly analogous to "Level 2" or "Level 3", with the distinction being the content of the repositories managed by the team.

{{note| As of June 30, 2016, all members of the Mozilla organization on GitHub '''MUST''' have [https://help.github.com/articles/about-two-factor-authentication/ 2FA enabled].|reminder}}

{{note| Automation accounts are also required to have 2FA enabled. Scripts should use [https://help.github.com/articles/creating-an-access-token-for-command-line-use/ access tokens] with minimum permissions to accomplish the task.}}


Some people are interested in being members of the Mozilla organization on GitHub as a way to highlight their contributions to the Mozilla Project. Thanks for your help! And there is a [https://www.mozilla.org/credits/ better place] to highlight your work. Please refer to the [https://www.mozilla.org/credits/FAQ FAQ] for that process.

=== Should I make a separate GitHub organization or just create a repository in an existing one? ===
This is a personal preference.  If you have a large enough project or organization feel free.  We suggest you use the strategies and recommendations here as a model to manage the details.

=== Forking vs Transferring ===
'''Do not "fork" a repository into a Mozilla organization.''' Doing so gives ''every team in the org'' rights to it.

If you have created a repo on your own account (for example, myuser/myrepo) and it should live under the Mozilla organization, here are the steps:

{{note|As soon as you transfer, your repository will be in "limbo" (only you will have write access) until you get the assistance of an [[#contact|org admin]] who can make the changes. Please plan in advance if timing is critical.}}

# If you're not a member of any team, talk to an [[#contact|org admin]].
# Under the repo admin, transfer ownership to the Mozilla organization. If you don't see this option, return to step 1.
# Choose which teams should be given access. All chosen teams will have only 'read' access at this point.
# Ask an [[#contact|org admin]] to grant team permissions higher than read ('write' and 'admin' are the other choices). (Team maintainers do not have the ability to change a repositories status.)
# Fork the repo from Mozilla (mozilla/myrepo) back to your account (recreating myuser/myrepo). While the transferred repo becomes the root of the network on GitHub (e.g. all forks are now forks of mozilla/myrepo) other users may be pointing to your repo by URL. (Optional, github will redirect old URLs for transfers, but you probably want a local repo if you use the PR workflow.)

=== Do I need to be an owner to create repositories? ===
No.  If a person has read/write access to another repository in that organization they can make more repositories in that organization. However, it's preferred that you create repositories in the context of a team.

=== Are there requirements for when or how I should create a new team? ===
No.  When requirements were proposed they all seemed too rigid and time consuming.  Instead we recommend staying flexible and using good naming and documentation for projects (similar to naming CSS classes or variables).

On large teams we recommend you separate teams for read/write and repository administration.

<div id="other_github"></div>
=== Is "mozilla" the only GitHub "organization" related to Mozilla? ===
No, there are plenty of Mozilla-related "organizations" on GitHub. As a rule of thumb, initiatives that create a large number of sub-repositories will create their own "organization". Here is a (probably incomplete) list of them:
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
