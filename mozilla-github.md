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

=== Posso ser um membro da Organização Mozilla? ===
Com as melhorias recentes do GitHub (2015), nós encorajamos (fortemente) seguir as diretrizes, que recomenda a criação de equipes no GitHub. Lembrando que, todos os membros da [https://github.com/mozilla/ Organização Mozilla no GitHub] concordam em serem vinculados ao [https://www.mozilla.org/en-US/about/governance/policies/commit/requirements/ Requisitos de Acesso para Submissão da Mozilla], como prática.
* "Colaborador externo": administradores do respositório podem conceder acesso para qualquer usuário que possua uma conta no GitHub como colaboradore externo. "Colaboradores externos" são análogos ao "Nível 1a" de acesso aos repositórios hospedados pela Mozilla.
* "Membros da equipe": Mantenedores de equipes podem adicionar usuários do GitHub a uma equipe, se eles já forem membros da organização. Se você ainda não é um membro da organização, o administrador da equipe deve [[#contact|requerer sua adição]] a sua equipe, como um atestado. "Membros de equipe" são análogos ao "Nível 2" ou "Nível 3", com a diferença sendo o repositório gerenciado pela equipe.
{{note| A partir de 30 de Junho de 2016, todos os membros da Organização Mozilla no GitHub '''DEVEM''' ter [https://help.github.com/articles/about-two-factor-authentication/ 2FA ativo].|lembrete}}

{{note| Contas para automação também devem ter 2FA ativo. Scripts devem utilizar [https://help.github.com/articles/creating-an-access-token-for-command-line-use/ tokens de acesso] com permissões mínimas somente para execução da tarefa.}}


Algumas pessoas estão interessadas em se tornar membros da Organização Mozilla no GitHub como uma forma de demonstrar suas contribuições com o Projeto Mozilla. Obrigado pela sua ajuda! E existe um [https://www.mozilla.org/credits/ lugar melhor] para demonstrar seu trabalho. Por favor verifique no [https://www.mozilla.org/credits/FAQ FAQ] sobre este processo.

=== Devo criar uma organização separada no GitHub ou somente criar um repositório em uma existente? ===
Esta é uma decisão pessoal. Se você tem um projeto ou uma organização grande o suficiente, sinta-se livre para escolher. Sugerimos usar as estratégias e recomendações neste documento como modelo para gerenciar os detalhes.

=== Forking vs Transferência ===
'''Não "fork" um repositório dentro de uma Organização Mozilla.''' Fazendo isso dá direito a ''todas as equipes na organização'' a fazerem também.

Se você criou um repositório na sua própria conta (por exemplo, meuusuario/meurepositorio) e isso deveria estar em uma Organização Mozilla, aqui estão os passos para isso:

{{note|Assim que você transferir, seu repositório estará no "limbo" (somente você terá acesso de escrita) até que você tenha assistência de um [[#contact|administrador da organização]] que possa realizar as alterações. Por favor planeje com antecedência se o tempo for crítico.}}


# Se vocẽ não é membro de nenhuma equipe, converse com um [[#contact|administrador da organização]].
# Dentro do repositório administrado, transfira a posse para a Organização Mozilla. Se vocẽ não conseguir ver esta opção, volte para o passo 1.
# Escolha quais equipes devem ser dadas acesso. Todas as equipes escolhidas terão somente acesso de leitura neste ponto.
# Peça a um [[#contact|administrador da organização]] para conceder permissões de acesso maior que leitura ('escrita' e 'admin' são outras opções). (Mantenedores de equipes não tem capacidade de mudar o estado de repositórios.)
# Fork o repositório da Mozilla (mozilla/meurepo) de volta para sua conta (recriando meuusuario/meurepo). Enquanto o repositório transferido se torna a base no GitHub (e.g. todos os forks são agora forks de mozilla/meurepo) outros usuários podem estar apontando para seu repositório pela URL. (Opcional, GitHub irá redirecionar URLs antigas para as transferências, mas você provavelmente deseja um repositório local se quiser usar o fluxo de PR.)

=== Eu preciso ser um dono para criar repositórios? ===
Não. Se uma pessoa tem acesso de leitura/escrita a outro repositório naquela organização elas podem criar mais repositórios nesta organização. No entanto, é recomendado que você crie repositório no contexto de equipe.

=== Existem requisitos para quando ou como eu devo criar uma nova equipe? ===
Não. Quando requisitos eram propostos eles pareciam muito rígidos e demorados. Em vez disso nós recomendamos manter a flexibilidade e utilização de boas nomeclaturas e documentação para projetos (semelhanças ao nomear classes CSS ou variáveis).

Em grandes equipes recomendamos que você separe equipes para leitura/escrita e administração dos repositórios.

<div id="other_github"></div>
=== "mozilla" é a única "organização" no GitHub referente a Mozilla? ===
Não, existem muitas "organizações" no GitHub relacionadas a Mozilla. Como princípio básico, iniciativas que criam um grande número de sub-repositórios criarão suas próprias "organizações". Aqui está (provavelmente incompleta) uma lista delas:
{| class="wikitable sortable"
|-
! Organização !! Descrição !! Contato do Responsável
|-
| [https://github.com/mozilla-it mozilla-it] || Repositórios da Mozilla IT || ?
|-
| [https://github.com/bugzilla bugzilla] || Bugzilla (o produto) || #bteam
|- 
| [https://github.com/drumbeat-badge-sprint drumbeat-badge-sprint] || Drumbeat Badge Lab || ?
|-
| [https://github.com/hackasaurus hackasaurus] || Hackasaurus || ?
|-
| [https://github.com/jetpack-labs jetpack-labs] || Jetpack Labs || ?
|-
| [https://github.com/mdn mdn] || Mozilla Developer Network || {{Mozillian|groovecoder|Luke Crouch}}
|-
| [https://github.com/mozbrick mozbrick] || Mozilla Brick (biblioteca de componentes web) || ?
|-
| [https://github.com/mozilla-appmaker mozilla-appmaker] || Mozilla Appmaker || ?
|-
| [https://github.com/mozilla-b2g mozilla-b2g] || Mozilla Boot2Gecko / Firefox OS || ?
|-
| [https://github.com/mozilla-bteam mozilla-bteam] || Bugzilla.Mozilla.org || #bteam
|-
| [https://github.com/mozilla-cit mozilla-cit] || Operações da Comunidade Mozilla || {{Mozillians|tanner|Tanner Filip}} or {{Mozillians|yalam96|Yousef Alam}}
|-
| [https://github.com/mozilla-comm mozilla-comm] || Projetos relacionados a Calendários e Mensagens || ?
|-
| [https://github.com/mozilla-cordova mozilla-cordova] || Suporte Firefox OS para Apache Cordova || ?
|-
| [https://github.com/mozilla-metrics mozilla-metrics] || Estísticas Mozilla || ?
|-
| [https://github.com/mozilla-raptor mozilla-raptor] || Desempenho Mozilla Raptor / Firefox OS || {{Mozillian|eliperelman|Eli Perelman}}, {{Mozillian|rwood|Rob Wood}}
|-
| [https://github.com/mozilla-releng mozilla-releng] || Engenharia de Lançamento Mozilla || #releng
|-
| [https://github.com/mozilla-services mozilla-services] || Serviços Mozilla || [https://github.com/orgs/mozilla-services/people?utf8=%E2%9C%93&query=role%3Aowner mozilla-services responsável]
|-
| [https://github.com/mozilla-svcops mozilla-svcops] || Operações dos Serviços em Nuvem Mozilla || {{Mozillian|relud|Daniel Thornton}}
|-
| [https://github.com/MozillaTW MozillaTW] || Mozilla Taiwan || ?
|-
| [https://github.com/Mozilla-TWQA Mozilla-TWQA] || Mozilla Taiwan QA || ?
|-
| [https://github.com/mozillahispano mozillahispano] || Mozilla Hispano || ?
|-
| [https://github.com/MozillaScience MozillaScience] || Mozilla Science Lab || ?
|-
| [https://github.com/MozillaSecurity MozillaSecurity] || Equipe da Plataforma de Fuzzing Mozilla master repo com muitas ferramentas de fuzzing disponíveis. || ?
|-
| [https://github.com/MozillaWiki MozillaWiki] || MozillaWiki (wiki.mozilla.org) || {{Mozillian|ckoehler|Christie Koehler}}, {{Mozillian|gphemsley|Gordon P. Hemsley}}
|-
| [https://github.com/mozillayvr mozillayvr] || Mozilla Vancouver @MozillaYVR || {{Mozillian|bclark|Brian Clark}}, {{Mozillian|shobson|Stephanie Hobson}}
|-
| [https://github.com/mozfr mozfr] || Mozilla Francófonos (falantes de Francês) || Pascal Chevrel https://mozillians.org/fr/u/pascalc/
|-
| [https://github.com/opennews opennews] || Novidades Cavaleiros-Mozilla || ?
|-
| [https://github.com/rust-lang rust-lang] || Linguagem de Programação Rust || {{Mozillian|aturon|Aaron Turon}}
|-
| [https://github.com/servo servo] || Servo (motor do navegador escrito em Rust) || {{Mozillian|larsberg|Lars Bergstrom}}, Jack Moffitt
|-
| [https://github.com/tabulapdf tabulapdf] || Projeto Tabula (extração de dados de arquivos PDF) || ?
|-
| [https://github.com/webcompat webcompat] || Equipe Compatibilidade Web || {{Mozillian|miketaylr|Mike Taylor}}
|-
| [https://github.com/mozilla-l10n mozilla-l10n] || Mozilla l10n-drivers equipe || Pascal Chevrel https://mozillians.org/fr/u/pascalc/
|-
| [https://github.com/taskcluster taskcluster] || [[TaskCluster]] Equipe || {{Mozillian|sdeckelmann|Selena Deckelmann}}
|-
| [https://github.com/MozillaCH MozillaCH] || Mozilla [[Switzerland]] || {{Mozillian|mkohler|Michael Kohler}}, {{Mozillian|freaktechnik|freaktechnik}}
|}

=== Existem outros repositórios não-oficiais ou repositórios relacionados a Mozilla no GitHub? ===
Sim! Sem ordem relacionada:

* [https://github.com/kinetiknz/nestegg/ https://github.com/kinetiknz/nestegg/] :  WebM demultiplexador
* [https://github.com/xiph/opus/ https://github.com/xiph/opus/] :  Compressão de áudio moderna para internet.
* [https://github.com/webmproject/libvpx https://github.com/webmproject/libvpx] :  Somente espelho. Por favor não envie _pull requests_.
* [https://github.com/campd/fxdt-adapters https://github.com/campd/fxdt-adapters] : Adaptadores de Protocolos para as Ferramentas para Desenvolvimento Firefox.
* [https://github.com/kripken/emscripten https://github.com/kripken/emscripten] :  Emscripten: Um compilador LLVM-para-JavaScript.
* [https://github.com/bbondy/codefirefox https://github.com/bbondy/codefirefox] :  Site com tutorial em vídeo e exercícios para desenvolver para Firefox e outras tecnologias relacionadas a Mozilla.
* [https://github.com/nickdesaulniers/where-is-firefox-os https://github.com/nickdesaulniers/where-is-firefox-os] :  Um mapa mostrando onde no mundo os telefones com Firefox OS foram vendidos.
* [https://github.com/jdm/bugsahoy https://github.com/jdm/bugsahoy] :  Uma página para tornar fácil o descobrimento de _bugs_ relevantes para novos contribuidores Mozilla.
* [https://github.com/w3c/web-platform-tests https://github.com/w3c/web-platform-tests] :  Suite de teste para especificações de plataformas Web.
* [https://github.com/w3c/wptserve https://github.com/w3c/wptserve] :  Um servidor Web desenvolvido para o uso com a Plataforma de testes para Web.
* [https://github.com/w3c/wptrunner https://github.com/w3c/wptrunner] : Executor multi-plataformas de testes para diferentes navegadores para testes de plataformas Web. Utilizado no mozilla-central e servo.
* [https://github.com/w3c/testharness.js https://github.com/w3c/testharness.js] : (sem descrição)
* [https://github.com/jdm/asknot https://github.com/jdm/asknot] :  Não pergunte o que a Mozilla pode fazer por você mas o quê você pode fazer pela Mozilla.
* [https://github.com/jeffbryner/MozDef https://github.com/jeffbryner/MozDef]: Plataforma Mozilla Defense.
* [https://github.com/jgraham/webdriver-rust https://github.com/jgraham/webdriver-rust]: Biblioteca WebDriver para Rust.
