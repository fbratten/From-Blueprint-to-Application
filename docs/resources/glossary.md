# Glossary of Terms

> Key terminology from "From Blueprint to Application"
>
> Entries marked *Svenska* add a plain-language Swedish explanation for beginners. Many of them come from the interactive AI Testing labs at [fbratten.github.io/labs](https://fbratten.github.io/labs/).

---

## A

<a id="term-agent"></a>**Agent** - An AI system that can take actions autonomously, make decisions, and work toward goals without constant human direction.


<a id="term-anchor"></a>**Anchor (Mutation Anchor)** - An exact piece of source code a mutation tool locates before deliberately changing a safety control. If the anchor moves or matches ambiguously, the gate must not silently report success.

*Svenska:* **mutationsankare** - En exakt plats i koden där ett mutationstest gör sin avsiktliga ändring. Om platsen inte hittas entydigt ska kontrollen slå larm, inte bli grön.
<a id="term-api"></a>**API (Application Programming Interface)** - The interface through which applications communicate with AI models.


<a id="term-artifact"></a>**Artifact (GitHub Actions)** - A file or package saved by a workflow run, for example a screenshot collection or a review preview. Artifacts have retention limits and are not proof that the underlying test passed.

*Svenska:* **En fil eller samling filer som sparas från ett CI-jobb, till exempel skärmbilder eller en testrapport. Artifakter kan upphöra att vara tillgängliga och visar inte i sig att testet lyckades.**
<a id="term-assertion"></a>**Assertion** - A statement in a test that must be true for the test to pass, e.g. "the score is a number between 0 and 1". An assertion written in a document or diagram is a requirement, not proof that anything was tested.

*Svenska:* **påstående (i ett test)** – En regel i ett test som måste stämma för att testet ska bli godkänt, t.ex. "poängen är ett tal mellan 0 och 1". Ett påstående som bara står i ett dokument eller en ritning är ett krav, inte ett bevis på att något har testats.

## B

<a id="term-backward-compatibility"></a>**Backward Compatibility** - When a new version of an API or data format still works for programs built for the old version. Compatibility checks catch changes that would break existing callers.

*Svenska:* **bakåtkompatibilitet** – En ny version av ett API eller dataformat fungerar fortfarande för program som byggts för den gamla versionen. Kontrollerna fångar ändringar som annars skulle få befintliga system att sluta fungera.

<a id="term-baseline"></a>**Baseline (Control-Present Run)** - The reference test run with the original control intact. A mutation result is meaningful only when the named tests actually run and pass on this baseline.

*Svenska:* **referenskörning** - Testkörningen med originalskyddet kvar. Testerna måste verkligen köras och lyckas här innan man kan tolka resultatet efter att skyddet saboterats.

<a id="term-branch"></a>**Branch** - An independent line of commits in Git. Work can be reviewed and tested on a branch without immediately changing the default integration branch such as main.

*Svenska:* **utvecklingsgren** - En egen utvecklingslinje med commits. Ändringar kan granskas och testas där utan att de omedelbart påverkar huvudgrenen main.

<a id="term-broken-mutation"></a>**BROKEN (Mutation Outcome)** - A mutation check whose result cannot be trusted: a test did not run on the baseline, setup failed, the source edit missed its anchor, or the mutant did not change the code. BROKEN is not a detected defect.

*Svenska:* **trasig mutationskontroll** - Kontrollen kunde inte ge ett tillförlitligt svar. Exempelvis kördes inte testet, testmiljön fallerade eller kodändringen träffade fel. Får inte räknas som en fångad mutation.

## C


<a id="term-caught-mutation"></a>**CAUGHT (Mutation Outcome)** - A deliberate defect was introduced, and the corresponding test failed in its test body while the baseline passed. This is evidence that the test detects that particular sabotage.

*Svenska:* **fångad mutation** - En avsiktlig försämring fick rätt test att fallera, medan originalkoden passerade. Det visar att testet reagerar på just den förändringen.
<a id="term-chain-of-thought"></a>**Chain-of-Thought (CoT)** - A prompting technique that encourages the AI to show its reasoning process step by step.


<a id="term-checkout"></a>**Checkout (GitHub Actions)** - Fetching an exact repository revision into a runner so the job executes or tests the intended source files. In an Actions workflow, actions/checkout is a reusable action that performs the checkout.

*Svenska:* **Att hämta en bestämd kodversion till den dator som kör testerna. actions/checkout är ett färdigt GitHub Actions-steg som gör detta.**
<a id="term-chunking"></a>**Chunking** - Splitting documents into smaller pieces ("chunks") before they are indexed for search in a RAG system. Poor chunking can cut sentences apart or separate a fact from its context.

*Svenska:* **uppdelning i textbitar** – Dokument delas upp i mindre stycken innan de läggs in för sökning i ett RAG-system. Delas texten fel kan en mening klippas av eller ett faktum hamna skilt från sitt sammanhang.

<a id="term-ci-cd"></a>**CI/CD (Continuous Integration / Continuous Delivery)** - Automated pipelines that build and test every code change (CI) and prepare or release approved changes (CD). In AI projects the same pipeline can also run evaluations of model output.

*Svenska:* **kontinuerlig integration och leverans** – Automatiska flöden som bygger och testar varje kodändring (CI) och förbereder eller släpper godkända ändringar (CD). I AI-projekt kan samma flöde även köra utvärderingar av modellens svar.


<a id="term-ci-job"></a>**CI Job** - One independently executed part of a CI workflow, such as unit tests, browser smoke checks or the mutation gate. A job contains one or more steps.

*Svenska:* **CI-jobb** - En separat kontrolluppgift i GitHub Actions, exempelvis vanliga tester eller Mutation Gate. Ett jobb består av flera arbetsmoment.

<a id="term-ci-step"></a>**CI Step** - A single action inside a CI job, such as checking out code, installing Python, installing a browser or running pytest.

*Svenska:* **CI-steg** - Ett enskilt moment i ett CI-jobb, exempelvis att hämta koden, installera Python eller köra ett testprogram.
<a id="term-circuit-breaker"></a>**Circuit Breaker** - A safety mechanism that stops a process when something keeps failing or repeating, for example an agent calling the same tool over and over. It stops the loop but does not fix the underlying cause.

*Svenska:* **kretsbrytare, nödstopp** – Ett skydd som stoppar en process när något upprepade gånger misslyckas eller går i loop, t.ex. en agent som anropar samma verktyg om och om igen. Det stoppar loopen men löser inte grundorsaken.


<a id="term-code-review"></a>**Code Review** - A review of proposed changes by another developer or reviewer. It can catch design defects, misleading assumptions and untested paths that an automated pipeline does not cover.

*Svenska:* **kodgranskning** - En annan utvecklare eller granskare bedömer föreslagna kodändringar. Det kan upptäcka felaktiga antaganden och testluckor som automatiska kontroller missar.
<a id="term-commit"></a>**Commit** - A saved, labelled snapshot of changes in a version control system such as Git. In CI, each commit can trigger a set of fast automated tests.

*Svenska:* **incheckning** – En sparad och märkt ögonblicksbild av ändringar i ett versionshanteringssystem som Git. I CI kan varje commit starta en uppsättning snabba automatiska tester.


<a id="term-commit-hash"></a>**Commit Hash (SHA)** - A long identifier for one exact Git commit. Using the full hash ties a review or test result to a precise revision rather than to a branch that may later move.

*Svenska:* **commit-hash eller SHA** - Ett långt ID för en exakt sparad kodversion. Det gör det möjligt att knyta tester och granskningar till rätt version även om en branch senare förändras.
<a id="term-context-window"></a>**Context Window** - The maximum amount of text (measured in tokens) that an AI model can process in a single interaction.

<a id="term-context-engineering"></a>**Context Engineering** - The practice of designing and managing the information provided to AI systems to optimize their outputs.

<a id="term-contract-test"></a>**Contract Test** - A test that checks that data exchanged between systems has the agreed shape: required fields, correct types and valid values. A valid shape says nothing about whether the content is true.

*Svenska:* **kontraktstest** – Kontrollerar att data som skickas mellan system har den överenskomna formen: rätt fält, rätt datatyper och giltiga värden. Rätt form säger inget om att innehållet är sant.

<a id="term-xss"></a>**Cross-Site Scripting (XSS)** - A browser security weakness in which untrusted text is interpreted as executable script, often after unsafe insertion into HTML. Escaping, validation and safe DOM APIs limit the risk.

*Svenska:* **skriptinjektion i webbläsaren** - En säkerhetsbrist där opålitlig text blir körbar webbkod, till exempel genom felaktig HTML-hantering. Korrekt escaping och säker DOM-hantering minskar risken.

## D

<a id="term-defense-in-depth"></a>**Defense in Depth** - Using several independent layers of protection, so that if one check misses a problem a later one may still catch it. No single layer is assumed to be perfect.

*Svenska:* **skydd i flera lager** – Flera oberoende skyddslager används, så att ett senare lager kan fånga det som ett tidigare missade. Inget enskilt lager antas vara perfekt.


<a id="term-deployment"></a>**Deployment** - Publishing a built application or website to a hosting environment. Deployment and passing CI checks are separate outcomes; after deployment, the public service can be tested again.

*Svenska:* **Att publicera en byggd applikation eller webbplats i en miljö där den ska användas. En grön testkörning och en lyckad publicering är två olika resultat som bör verifieras var för sig.**
<a id="term-deterministic-test"></a>**Deterministic Test** - A test that gives the same result every time for the same input, such as a format or permission check. Deterministic tests are fast and cheap, unlike sampled AI evaluations whose results can vary.

*Svenska:* **deterministiskt test** – Ger alltid samma resultat för samma indata, t.ex. en kontroll av format eller behörigheter. Sådana tester är snabba och billiga, till skillnad från stickprovsbaserade AI-utvärderingar där resultaten kan variera.


<a id="term-diff"></a>**Diff** - The comparison of two code versions showing added, removed and changed lines. Reviewing a diff helps establish the precise change scope and spot accidental losses.

*Svenska:* **ändringsjämförelse** - En jämförelse av två kodversioner som visar tillagda, borttagna och ändrade rader. Används för att hitta oavsiktliga förändringar före merge.
<a id="term-drift"></a>**Drift** - A gradual change after release, in data, user behaviour or model output, that can make a system perform worse than when it was tested. Drift is detected by monitoring live use over time.

*Svenska:* **glidning (drift)** – Gradvisa förändringar efter lansering, i data, användarbeteende eller modellens svar, som kan göra att systemet fungerar sämre än när det testades. Upptäcks genom att man följer den verkliga användningen över tid. Obs: inte samma sak som svenskans "drift" i betydelsen att driva och underhålla system.

## E

<a id="term-end-to-end-test"></a>**End-to-End Test (E2E)** - A test that runs a complete user journey through the whole system, for example in a browser, to confirm that all parts work together. One passing run does not guarantee future reliability.

*Svenska:* **helhetstest** – Testar ett helt användarflöde genom hela systemet, t.ex. i en webbläsare, för att se att alla delar fungerar ihop. Att det gick bra en gång garanterar inte att det fortsätter att fungera.

<a id="term-escaped-mutation"></a>**ESCAPED (Mutation Outcome)** - A deliberate defect was introduced but the named test did not fail as expected. The test may miss the control, exercise another guard or be too weak. ESCAPED signals a test gap, not necessarily an observed production exploit.

*Svenska:* **mutation som slank igenom** - Skyddet försämrades utan att rätt test slog larm. Det visar en lucka i testernas förmåga, men bevisar inte i sig ett verkligt angrepp i produktion.

## F

<a id="term-fail-closed"></a>**Fail Closed** - A design choice where a system blocks an action when a check fails or is uncertain, instead of letting it through. The opposite, "fail open", lets the action proceed.

*Svenska:* **stäng vid fel** – Systemet stoppar en handling när en kontroll misslyckas eller är osäker, i stället för att släppa igenom den. Motsatsen, "fail open", låter handlingen gå vidare.

<a id="term-fault-injection"></a>**Fault Injection** - Deliberately introducing a known error, such as a malicious instruction or a broken data format, to see whether the system's checks catch it.

*Svenska:* **felinjicering** – Man lägger medvetet in ett känt fel, t.ex. en skadlig instruktion eller ett trasigt dataformat, för att se om systemets kontroller fångar det.

<a id="term-few-shot-learning"></a>**Few-Shot Learning** - Providing examples in the prompt to help the AI understand the desired output format or style.

<a id="term-fine-tuning"></a>**Fine-Tuning** - Customizing a pre-trained AI model with additional training data for specific use cases.

<a id="term-fixture"></a>**Fixture** - A fixed, prepared test input or setup that makes a test run the same way every time. A "healthy" fixture is a normal case; a fault fixture contains a known error.

*Svenska:* **förberedd testdata** – Förberedd och oförändrad indata eller miljö som gör att ett test körs likadant varje gång. En "frisk" fixture är ett normalfall, en felfixture innehåller ett känt fel.

## G


<a id="term-git"></a>**Git** - A version-control system that records file history as commits and supports branches, comparisons and merges. Git is the tool; GitHub is a service that hosts repositories and collaboration.

*Svenska:* **Git versionshantering** - Systemet som spårar ändringar i filer och skapar commits, branches och merges. Git är verktyget; GitHub är en tjänst som kan lagra och samordna Git-repon.

<a id="term-github-actions"></a>**GitHub Actions** - GitHub's automation service that executes configured workflows when events such as a push occur. Test jobs run on runners and report their results against a specific commit.

*Svenska:* **GitHub Actions** - GitHubs tjänst för automatisering. När exempelvis en push görs kan den starta definierade testjobb och redovisa resultat för en bestämd commit.

<a id="term-github-pages"></a>**GitHub Pages** - GitHub's static website hosting service. A workflow can build a site, deploy it to GitHub Pages and run browser checks against the public URL.

*Svenska:* **GitHubs tjänst för att publicera statiska webbplatser. Ett workflow kan bygga sidorna, publicera dem och därefter testa den publika webbadressen.**
<a id="term-golden-dataset"></a>**Golden Dataset** - A versioned collection of example inputs with expected or approved answers, used to check whether a change to a prompt, model or retrieval step made results worse. A small set cannot cover every real-world case.

*Svenska:* **referensdataset, facit** – En versionshanterad samling exempelfrågor med förväntade eller godkända svar. Används för att se om en ändring av prompt, modell eller sökning har försämrat resultaten. En liten samling täcker aldrig alla verkliga fall.

<a id="term-groundedness"></a>**Groundedness** - Whether each claim in an AI answer is supported by the source material the model was given. A groundedness check can hold back unsupported claims, but it does not catch every factual error.

*Svenska:* **förankring i källor** – Om varje påstående i ett AI-svar faktiskt stöds av källmaterialet som modellen fick. En sådan kontroll kan hålla tillbaka påståenden utan stöd, men fångar inte alla faktafel.


<a id="term-guard"></a>**Guard (Safety Check)** - A conditional check in code that rejects or delays an unsafe action, for example refusing malformed IDs or blocking updates while a dialog is open. A documented guard is not proof that it runs.

*Svenska:* **skyddskontroll** - En villkorskontroll i programkod som stoppar ett olämpligt steg, till exempel felaktiga ID:n. Att kontrollen finns i koden bevisar inte att den faktiskt nås vid körning.
<a id="term-guardrail"></a>**Guardrail** - A rule or check placed around an AI model to block unwanted input or output, such as injection attempts or sensitive data. A guardrail that is described or configured has not necessarily been shown to work.

*Svenska:* **skyddsräcke** – En regel eller kontroll runt en AI-modell som stoppar oönskad indata eller utdata, t.ex. injektionsförsök eller känsliga uppgifter. Att ett skydd finns beskrivet eller inställt betyder inte att det har visats fungera.

## H

<a id="term-hallucination"></a>**Hallucination** - When an AI generates false or fabricated information that appears plausible.

<a id="term-handoff"></a>**Handoff** - The point where one agent, service or person passes a task and its context to another. Handoff tests check that context is not lost and that ownership is clear; a delivered message is not a completed task.

*Svenska:* **överlämning** – När en agent, tjänst eller person lämnar över en uppgift med dess sammanhang till en annan. Tester kontrollerar att inget sammanhang tappas och att det är tydligt vem som äger uppgiften. Ett levererat meddelande är inte en utförd uppgift.


<a id="term-headless-browser"></a>**Headless Browser** - A real browser engine running without a visible window. Browser tests can still click elements, send keyboard input and observe page behaviour, including JavaScript errors.

*Svenska:* **webbläsare utan synligt fönster** - En riktig webbläsarmotor som körs automatiskt utan att något fönster visas. Tester kan ändå klicka, skriva och kontrollera gränssnittets beteende.

<a id="term-html-escaping"></a>**HTML Escaping** - Converting characters such as angle brackets and quotes into safe text representations before inserting untrusted content into HTML. The correct escaping depends on the context, for example text versus attributes.

*Svenska:* **HTML-escaping** - Att göra specialtecken i opålitlig text ofarliga innan de placeras i HTML. Tecken i HTML-attribut kan kräva annan hantering än vanlig text.
<a id="term-human-in-the-loop"></a>**Human-in-the-Loop (HITL)** - A setup where a person must review or approve certain AI actions, such as writing or changing data, before they take effect.

*Svenska:* **människa i loopen** – En person måste granska eller godkänna vissa AI-handlingar, t.ex. att skriva eller ändra data, innan de genomförs.

## I

<a id="term-integration-test"></a>**Integration Test** - A test that checks that several components work correctly together, for example an application, its database and a message queue. Passing in a test environment does not prove the same in production.

*Svenska:* **integrationstest** – Kontrollerar att flera delar fungerar ihop, t.ex. en applikation, dess databas och en meddelandekö. Att det fungerar i testmiljön bevisar inte att det fungerar i produktion.

## L

<a id="term-least-privilege"></a>**Least Privilege** - Giving a user, service or agent only the permissions it needs for its task and nothing more, often enforced with an allowlist of permitted actions.

*Svenska:* **minsta möjliga behörighet** – En användare, tjänst eller agent får bara de rättigheter den behöver för sin uppgift, ofta styrt med en lista över tillåtna handlingar (allowlist).

<a id="term-linting"></a>**Linting** - Automatic checking of code for syntax errors, style problems and likely mistakes without running it. Often combined with type checking under the name "static checks". Passing a linter does not prove that the program behaves correctly.

*Svenska:* **automatisk kodkontroll (lintning)** – Automatisk kontroll av kod efter syntaxfel, stilproblem och troliga misstag, utan att koden körs. Kombineras ofta med typkontroll under namnet statiska kontroller. Godkänd lintning bevisar inte att programmet beter sig rätt.

<a id="term-llm-as-a-judge"></a>**LLM-as-a-Judge** - Using a language model to score or grade another model's answers. Cheaper "fast judges" can check samples often, while more thorough "deep judges" run less often. A model judge can disagree with qualified human reviewers.

*Svenska:* **AI-modell som bedömare** – En språkmodell används för att poängsätta eller bedöma en annan modells svar. Snabba och billigare bedömare kan köras ofta på stickprov, medan grundligare bedömare körs mer sällan. En AI-bedömare kan göra en annan bedömning än en kunnig människa.

## M

<a id="term-mcp"></a>**MCP (Model Context Protocol)** - A standardized protocol for connecting AI models to external tools and data sources.

<a id="term-merge"></a>**Merge (Git)** - Integrating changes from one branch into another after review and checks. A merge changes the target branch; it is different from merely pushing commits to a review branch.

*Svenska:* **sammanfogning av utvecklingsgrenar** - Ändringar från en branch förs in i en annan efter kontroller och granskning. En merge påverkar målgrenen, till skillnad från en vanlig push.

<a id="term-mock"></a>**Mock** - A simplified stand-in for a real component, such as a fake database or API, used in tests. Mocks make tests fast but can hide real integration problems.

*Svenska:* **låtsaskomponent, attrapp** – En förenklad ersättare för en riktig del, t.ex. en låtsasdatabas eller ett låtsas-API, som används i tester. Gör testerna snabba men kan dölja verkliga problem i samspelet mellan delarna.

<a id="term-multi-agent-system"></a>**Multi-Agent System** - Multiple AI agents working together, each with specialized roles and capabilities.

<a id="term-mutation"></a>**Mutation (Software Testing)** - A small, deliberate change to program code that removes or weakens behaviour, such as replacing a safety check with a constant. It is applied to a temporary test copy, not production.

*Svenska:* **mutation i mjukvarutest** - En liten avsiktlig kodförändring som försämrar ett beteende, exempelvis tar bort en spärr. Den görs i en tillfällig testkopia, inte i produktionskoden.

<a id="term-mutation-gate"></a>**Mutation Gate** - A CI checkpoint that requires mutation tests to prove that known safety controls are observable. In tachylite-mcp a pass requires both a green baseline and a caught failure after each mutation.

*Svenska:* **mutationsgrind** - En kontrollpunkt i CI som visar att testerna märker när kända skyddsabeteenden förstörs. Originalkoden ska passera, och den avsiktligt försämrade versionen ska få rätt test att fallera.

<a id="term-mutation-testing"></a>**Mutation Testing** - A method for testing the tests: deliberately change the code and see whether relevant tests fail. The result measures sensitivity to selected changes, not the absence of all possible bugs.

*Svenska:* **mutationstestning** - En metod för att testa själva testerna: ändra koden avsiktligt och se om rätt tester märker felet. Den bevisar inte att alla tänkbara fel upptäcks.

## N

<a id="term-nightly-run"></a>**Nightly Run** - A larger, scheduled test run, typically overnight, that covers the full evaluation set instead of a sample. It complements the quick checks run on each commit.

*Svenska:* **nattlig testkörning** – En större schemalagd testkörning, ofta nattetid, som går igenom hela utvärderingssamlingen i stället för ett stickprov. Kompletterar de snabba kontrollerna vid varje commit.

<a id="term-non-vacuous-test"></a>**Non-Vacuous Test** - A test that can fail for the property it claims to check. For example, after rejecting malformed updates, it also accepts a valid update over the same channel rather than passing because all updates are blocked.

*Svenska:* **icke-vakuöst test** - Ett test som verkligen kan avslöja det avsedda felet. Om felaktiga uppdateringar nekas måste testet även visa att en korrekt uppdatering fungerar, så att ett helt avstängt system inte ger falskt grönt.

## O

<a id="term-opt-in"></a>**Opt-In** - A feature stays disabled until the user explicitly chooses to enable it. A secure opt-in needs enforcement, not just a switch or indicator that says it is off.

*Svenska:* **aktivt tillval** - En funktion är avstängd tills användaren själv slår på den. Det måste också finnas en fungerande spärr i koden, inte bara en knapp som säger av.

## P


<a id="term-pipeline"></a>**Pipeline** - An ordered or parallel sequence of automated build, test, evaluation and release tasks. A green pipeline reports the checks it ran, not universal correctness.

*Svenska:* **automatiserat arbetsflöde** - En följd av automatiska moment för byggning, test och eventuell leverans. Ett grönt flöde bevisar bara de kontroller som faktiskt ingick.

<a id="term-playwright"></a>**Playwright** - A browser automation and testing toolkit. A test can open an actual Chromium-based browser, navigate pages, click controls, inspect visible elements and check mobile layout.

*Svenska:* **Ett verktyg för att styra webbläsare automatiskt vid tester. Det kan öppna sidor, klicka, kontrollera menyer och verifiera hur en webbplats ser ut på mobil.**
<a id="term-prompt"></a>**Prompt** - The input text or instructions given to an AI model.

<a id="term-prompt-engineering"></a>**Prompt Engineering** - The systematic practice of designing, optimizing, and refining prompts to achieve desired AI outputs.

<a id="term-prompt-injection"></a>**Prompt Injection** - A security vulnerability where malicious instructions are hidden within input to manipulate AI behavior.

<a id="term-prompt-library"></a>**Prompt Library** - A centralized collection of tested, optimized prompts for organizational use.

<a id="term-pull-request"></a>**Pull Request (PR)** - A request to merge a set of code changes into the main code base, where others can review the changes and automated tests run before they are accepted.

*Svenska:* **ändringsförfrågan** – En begäran om att föra in ändringar i huvudkoden, där andra kan granska dem och automatiska tester körs innan de godkänns.

<a id="term-push"></a>**Push (Git)** - The operation that uploads local Git commits to a remote repository such as GitHub. Pushing a review branch does not merge it into main.

*Svenska:* **publicering av commits** - Att skicka lokala commits till ett fjärrrepo, exempelvis GitHub. En push av en arbetsbranch är inte samma sak som att merga till main.

<a id="term-pytest"></a>**Pytest** - A Python test framework that runs test functions and reports whether they passed, failed, were skipped or could not run. An assertion inside a test checks expected behaviour.

*Svenska:* **Pytest** - Ett testverktyg för Python som kör testfunktioner och rapporterar om de lyckades, misslyckades eller hoppades över.

## R

<a id="term-rag"></a>**RAG (Retrieval-Augmented Generation)** - A technique that enhances AI responses by retrieving relevant information from external sources.

<a id="term-recall-k"></a>**Recall@k** - A search metric: the share of the relevant documents that appear among the top k results. A high score shows that the right material was found, not that the final answer is true.

*Svenska:* **andel relevanta träffar bland de k första** – Ett mått för sökning: hur stor del av de relevanta dokumenten som finns bland de k översta träffarna. Ett högt värde visar att rätt material hittades, inte att det slutliga svaret är sant.

<a id="term-red-teaming"></a>**Red Teaming** - Deliberately attacking your own system, as an adversary would, to find weaknesses. Saved attacks can be re-run as regression tests, but passing them does not prove that the system is secure in general.

*Svenska:* **angreppstester (red teaming)** – Man angriper medvetet sitt eget system som en motståndare skulle göra, för att hitta svagheter. Sparade attacker kan köras igen som regressionstester, men att klara dem bevisar inte att systemet är säkert i allmänhet.

<a id="term-regression-test"></a>**Regression Test** - A test that is re-run after changes to make sure that something which used to work has not broken. In AI systems this often means re-running the golden dataset after changing a prompt, model or retrieval step.

*Svenska:* **regressionstest** – Ett test som körs om efter ändringar för att se att något som fungerade tidigare inte har gått sönder. I AI-system betyder det ofta att man kör om referensdatasetet efter att ha ändrat prompt, modell eller sökning.


<a id="term-repository"></a>**Repository (Repo)** - A project store managed with Git: files, code, documentation and commit history. A repository can have several branches, but a branch is not another repository.

*Svenska:* **repository eller repo** - En versionshanterad projektförvaring med filer, kod, dokumentation och historik. Ett repo kan ha flera branches, men en branch är inte ett nytt repo.
<a id="term-retrieval"></a>**Retrieval** - The search step in a RAG system that finds passages to give the model before it answers. Retrieval is tested separately from the answer, because weak or irrelevant passages lead to weak answers.

*Svenska:* **hämtning, sökning** – Söksteget i ett RAG-system som letar fram textstycken åt modellen innan den svarar. Testas separat från svaret, eftersom svaga eller irrelevanta träffar ger svaga svar.

<a id="term-role-prompting"></a>**Role Prompting** - Assigning a specific persona or expertise to the AI (e.g., "You are an expert technical writer").

<a id="term-rollback"></a>**Rollback** - Restoring the previous valid state after a failed operation. For a visual canvas, a failed incoming update must not leave an unusable or partly replaced graph behind.

*Svenska:* **återställning** - Att gå tillbaka till ett tidigare fungerande tillstånd efter ett misslyckande. Om en inkommande uppdatering inte kan ritas ska den tidigare arbetsytan finnas kvar.


<a id="term-run-trigger"></a>**Run Trigger (GitHub Actions)** - The event or manual request that starts a workflow run. push, pull_request and workflow_dispatch may select different conditional steps inside the same workflow.

*Svenska:* **Den händelse som startar ett workflow. Exempel är en push, en pull request eller manuell start. Samma workflow kan då välja olika steg.**
<a id="term-runner"></a>**Runner (GitHub Actions)** - The computer or temporary virtual environment that executes a CI job. Using a fresh runner helps show that tests also work outside the developer's own machine.

*Svenska:* **testkörningsmiljö** - Den dator eller tillfälliga virtuella miljö som utför ett CI-jobb. En ren runner hjälper till att upptäcka beroenden till utvecklarens egen dator.

## S

<a id="term-sampled-evaluation"></a>**Sampled Evaluation** - Checking a random selection of test cases instead of all of them, to save time and cost. Sampling gives quick feedback but can miss problems in the cases that were not selected.

*Svenska:* **stickprovsutvärdering** – Man kontrollerar ett slumpmässigt urval av testfallen i stället för alla, för att spara tid och pengar. Ger snabb återkoppling men kan missa problem i de fall som inte kom med.

<a id="term-sandbox"></a>**Sandbox** - An isolated environment where code or agent actions can be tried without affecting real systems or data.

*Svenska:* **sandlåda, testmiljö** – En avskild miljö där kod eller agenthandlingar kan provas utan att påverka riktiga system eller data.

<a id="term-schema"></a>**Schema** - A formal description of what data must look like: which fields exist, which are required and what type each value has (e.g. JSON Schema).

*Svenska:* **schema, datamall** – En formell beskrivning av hur data ska se ut: vilka fält som finns, vilka som är obligatoriska och vilken typ varje värde ska ha (t.ex. JSON Schema).

<a id="term-short-circuit"></a>**Short-Circuit (Early Exit)** - Stopping a test run as soon as a cheap check fails, so that more expensive checks, such as model-based evaluation, are not run unnecessarily.

*Svenska:* **tidigt avbrott** – En testkörning stoppas så fort en billig kontroll misslyckas, så att dyrare kontroller, t.ex. AI-baserad utvärdering, inte körs i onödan.


<a id="term-smoke-test"></a>**Smoke Test** - A quick end-to-end check that a key feature starts and performs a representative action. A UI smoke test may open the page in a browser and simulate clicks or typing.

*Svenska:* **röktest eller snabbtest** - En kort kontroll av att viktiga funktioner över huvud taget fungerar. Ett UI-smoke-test öppnar exempelvis sidan i en webbläsare och provar användarhandlingar.

<a id="term-state-mirror"></a>**State Mirror (Live Mirror)** - A feature that applies incoming stateChanged messages to an open graphical canvas. When it is off, execution events may still arrive without replacing the user's graph.

*Svenska:* **direktspegling av tillstånd** - En funktion som uppdaterar en öppen grafisk arbetsyta när nya tillstånd kommer in. Den kan vara avstängd samtidigt som körstatus fortsätter visas.
<a id="term-system-prompt"></a>**System Prompt** - Instructions that define the AI's behavior across an entire conversation, typically set by the application developer.

## T

<a id="term-temperature"></a>**Temperature** - A parameter controlling the randomness/creativity of AI outputs (lower = more deterministic, higher = more creative).

<a id="term-test-gate"></a>**Test Gate** - A checkpoint in a pipeline that a change or request must pass before it moves on. If the check fails, the change is stopped, retried or sent for review.

*Svenska:* **kontrollpunkt (testgrind)** – En kontrollpunkt i ett flöde som en ändring eller förfrågan måste passera för att gå vidare. Om kontrollen inte går igenom stoppas ändringen, görs om eller skickas till granskning.


<a id="term-test-harness"></a>**Test Harness** - The surrounding test machinery that prepares copies, fixtures, browsers and checks before and after running tests. If the harness itself is broken, a green-looking result may be meaningless.

*Svenska:* **testhärva eller testmiljöapparat** - Koden och verktygen runt testerna som sätter upp testdata och miljö, kör kontroller och samlar resultat. Även dessa verktyg måste kunna verifieras.

<a id="term-test-matrix"></a>**Test Matrix** - Running equivalent tests under several selected environments, such as different Python versions. Each matrix job must report its own result; one version passing does not prove the others.

*Svenska:* **testmatris** - Samma tester körs i flera miljöer, exempelvis olika Pythonversioner. Varje kombination måste ha ett eget redovisat resultat.
<a id="term-threat-model"></a>**Threat Model** - A structured review of what needs protecting, who might misuse the system and where untrusted data crosses into trusted parts (trust boundaries). It guides which protections to build but enforces nothing by itself.

*Svenska:* **hotmodell** – En genomgång av vad som behöver skyddas, vem som kan missbruka systemet och var opålitlig data passerar in i betrodda delar (förtroendegränser). Den visar vilka skydd som behövs men skyddar ingenting i sig.

<a id="term-token"></a>**Token** - The basic unit of text processing for AI models. Roughly 4 characters or 3/4 of a word in English.

<a id="term-tool-use"></a>**Tool Use** - The ability of AI models to call external functions or APIs to accomplish tasks.

<a id="term-trace"></a>**Trace** - A recorded log of the steps a system took for one request, such as which documents were retrieved, which tools were called and what the model answered. Traces from live use are needed to judge quality after release.

*Svenska:* **spårlogg** – En sparad logg över stegen systemet tog för en förfrågan, t.ex. vilka dokument som hämtades, vilka verktyg som anropades och vad modellen svarade. Spår från verklig användning behövs för att bedöma kvaliteten efter lansering.

## U

<a id="term-unit-test"></a>**Unit Test** - A small, fast test of one piece of code in isolation, such as a single function, including edge cases and error handling.

*Svenska:* **enhetstest** – Ett litet, snabbt test av en enskild koddel, t.ex. en funktion, inklusive gränsfall och felhantering.

<a id="term-untrusted-content"></a>**Untrusted Content** - Any text the system did not write itself, such as user input, web pages or retrieved documents. It should be treated as data, never as instructions, because it may contain prompt injection.

*Svenska:* **opålitligt innehåll** – All text som systemet inte själv har skrivit, t.ex. användarinmatning, webbsidor eller hämtade dokument. Ska behandlas som data och aldrig som instruktioner, eftersom den kan innehålla promptinjektion.

## V


<a id="term-validator"></a>**Validator** - Code that checks incoming data against expected shapes, types and values before the data is used. It should reject malformed inputs for the right reason while accepting legitimate ones.

*Svenska:* **indatakontroll** - Kod som kontrollerar datas form, typ och värden innan de används. Den ska neka felaktig data men samtidigt tillåta korrekt data.
<a id="term-verification-receipt"></a>**Verification Receipt** - A record of what a check actually examined and what it found, kept as evidence. A statement such as "change completed" is only a claim; the receipt is what lets someone verify it.

*Svenska:* **verifieringskvitto** – En sparad uppgift om vad en kontroll faktiskt undersökte och kom fram till. Ett påstående som "ändringen är klar" är bara ett påstående; kvittot gör att någon kan kontrollera det.

## W

<a id="term-websocket"></a>**WebSocket** - A persistent two-way connection between a browser and a server. In tachylite-mcp, stateChanged and executionEvent messages share the connection but have different handling rules.

*Svenska:* **WebSocket-förbindelse** - En tvåvägskanal mellan webbläsare och server som kan skicka meddelanden direkt utan att öppna en ny anslutning varje gång.

<a id="term-workflow"></a>**Workflow (Automation)** - A defined sequence of tasks. In GitHub Actions, a workflow is configured in a YAML file and contains jobs and steps; in Tachylite it can also mean the node graph being edited.

*Svenska:* **arbetsflöde** - En beskriven följd av uppgifter. I GitHub Actions är det en YAML-fil med jobb och steg; i Tachylite kan ordet också betyda den graf med noder som användaren redigerar.


<a id="term-workflow-dispatch"></a>**Workflow Dispatch** - A GitHub Actions event that lets an authorized person or automation start a workflow explicitly rather than waiting for a push or pull request.

*Svenska:* **Ett sätt att uttryckligen starta ett GitHub Actions-workflow, manuellt eller genom ett godkänt anrop, utan att vänta på en ny kodändring.**

<a id="term-workflow-run"></a>**Workflow Run** - One particular execution of a configured workflow. Each run has its own run ID, event, commit SHA, outcome, jobs and logs; it differs from the reusable workflow definition.

*Svenska:* **En bestämd körning av ett workflow. Varje körning har ett eget körnings-ID, en kodversion, en starthändelse, jobb, loggar och resultat. Själva workflow-filen är receptet, inte en körning.**
<a id="term-worktree"></a>**Worktree (Git)** - A separate checkout directory belonging to an existing Git repository. It lets different branches be worked on in isolated folders without overwriting each other's uncommitted files.

*Svenska:* **separat arbetsmapp i Git** - En extra utcheckad projektmapp knuten till samma Git-repo. Den isolerar arbetet med en branch så andra arbetsmappars osparade ändringar inte påverkas.

## Y

<a id="term-yaml"></a>**YAML** - A human-readable configuration format. GitHub Actions workflows are stored as YAML files in .github/workflows and declare event triggers, job permissions, steps and conditions.

*Svenska:* **Ett textformat för inställningar. GitHub Actions använder YAML-filer under .github/workflows för att beskriva när kontroller körs, vilka jobb som ingår och vad de ska göra.**

## Z

<a id="term-zero-shot"></a>**Zero-Shot** - Asking an AI to perform a task without providing examples in the prompt.

---

[← Back to Resources](../README.md)
