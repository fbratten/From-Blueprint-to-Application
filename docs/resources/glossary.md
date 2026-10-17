# Glossary of Terms

> Key terminology from "From Blueprint to Application"
>
> Entries marked *Svenska* add a plain-language Swedish explanation for beginners. Many of them come from the interactive AI Testing labs at [fbratten.github.io/labs](https://fbratten.github.io/labs/).

---

## A

**Agent** - An AI system that can take actions autonomously, make decisions, and work toward goals without constant human direction.

**API (Application Programming Interface)** - The interface through which applications communicate with AI models.

**Assertion** - A statement in a test that must be true for the test to pass, e.g. "the score is a number between 0 and 1". An assertion written in a document or diagram is a requirement, not proof that anything was tested.

*Svenska:* **påstående (i ett test)** – En regel i ett test som måste stämma för att testet ska bli godkänt, t.ex. "poängen är ett tal mellan 0 och 1". Ett påstående som bara står i ett dokument eller en ritning är ett krav, inte ett bevis på att något har testats.

## B

**Backward Compatibility** - When a new version of an API or data format still works for programs built for the old version. Compatibility checks catch changes that would break existing callers.

*Svenska:* **bakåtkompatibilitet** – En ny version av ett API eller dataformat fungerar fortfarande för program som byggts för den gamla versionen. Kontrollerna fångar ändringar som annars skulle få befintliga system att sluta fungera.

## C

**Chain-of-Thought (CoT)** - A prompting technique that encourages the AI to show its reasoning process step by step.

**Chunking** - Splitting documents into smaller pieces ("chunks") before they are indexed for search in a RAG system. Poor chunking can cut sentences apart or separate a fact from its context.

*Svenska:* **uppdelning i textbitar** – Dokument delas upp i mindre stycken innan de läggs in för sökning i ett RAG-system. Delas texten fel kan en mening klippas av eller ett faktum hamna skilt från sitt sammanhang.

**CI/CD (Continuous Integration / Continuous Delivery)** - Automated pipelines that build and test every code change (CI) and prepare or release approved changes (CD). In AI projects the same pipeline can also run evaluations of model output.

*Svenska:* **kontinuerlig integration och leverans** – Automatiska flöden som bygger och testar varje kodändring (CI) och förbereder eller släpper godkända ändringar (CD). I AI-projekt kan samma flöde även köra utvärderingar av modellens svar.

**Circuit Breaker** - A safety mechanism that stops a process when something keeps failing or repeating, for example an agent calling the same tool over and over. It stops the loop but does not fix the underlying cause.

*Svenska:* **kretsbrytare, nödstopp** – Ett skydd som stoppar en process när något upprepade gånger misslyckas eller går i loop, t.ex. en agent som anropar samma verktyg om och om igen. Det stoppar loopen men löser inte grundorsaken.

**Commit** - A saved, labelled snapshot of changes in a version control system such as Git. In CI, each commit can trigger a set of fast automated tests.

*Svenska:* **incheckning** – En sparad och märkt ögonblicksbild av ändringar i ett versionshanteringssystem som Git. I CI kan varje commit starta en uppsättning snabba automatiska tester.

**Context Window** - The maximum amount of text (measured in tokens) that an AI model can process in a single interaction.

**Context Engineering** - The practice of designing and managing the information provided to AI systems to optimize their outputs.

**Contract Test** - A test that checks that data exchanged between systems has the agreed shape: required fields, correct types and valid values. A valid shape says nothing about whether the content is true.

*Svenska:* **kontraktstest** – Kontrollerar att data som skickas mellan system har den överenskomna formen: rätt fält, rätt datatyper och giltiga värden. Rätt form säger inget om att innehållet är sant.

## D

**Defense in Depth** - Using several independent layers of protection, so that if one check misses a problem a later one may still catch it. No single layer is assumed to be perfect.

*Svenska:* **skydd i flera lager** – Flera oberoende skyddslager används, så att ett senare lager kan fånga det som ett tidigare missade. Inget enskilt lager antas vara perfekt.

**Deterministic Test** - A test that gives the same result every time for the same input, such as a format or permission check. Deterministic tests are fast and cheap, unlike sampled AI evaluations whose results can vary.

*Svenska:* **deterministiskt test** – Ger alltid samma resultat för samma indata, t.ex. en kontroll av format eller behörigheter. Sådana tester är snabba och billiga, till skillnad från stickprovsbaserade AI-utvärderingar där resultaten kan variera.

**Drift** - A gradual change after release, in data, user behaviour or model output, that can make a system perform worse than when it was tested. Drift is detected by monitoring live use over time.

*Svenska:* **glidning (drift)** – Gradvisa förändringar efter lansering, i data, användarbeteende eller modellens svar, som kan göra att systemet fungerar sämre än när det testades. Upptäcks genom att man följer den verkliga användningen över tid. Obs: inte samma sak som svenskans "drift" i betydelsen att driva och underhålla system.

## E

**End-to-End Test (E2E)** - A test that runs a complete user journey through the whole system, for example in a browser, to confirm that all parts work together. One passing run does not guarantee future reliability.

*Svenska:* **helhetstest** – Testar ett helt användarflöde genom hela systemet, t.ex. i en webbläsare, för att se att alla delar fungerar ihop. Att det gick bra en gång garanterar inte att det fortsätter att fungera.

## F

**Fail Closed** - A design choice where a system blocks an action when a check fails or is uncertain, instead of letting it through. The opposite, "fail open", lets the action proceed.

*Svenska:* **stäng vid fel** – Systemet stoppar en handling när en kontroll misslyckas eller är osäker, i stället för att släppa igenom den. Motsatsen, "fail open", låter handlingen gå vidare.

**Fault Injection** - Deliberately introducing a known error, such as a malicious instruction or a broken data format, to see whether the system's checks catch it.

*Svenska:* **felinjicering** – Man lägger medvetet in ett känt fel, t.ex. en skadlig instruktion eller ett trasigt dataformat, för att se om systemets kontroller fångar det.

**Few-Shot Learning** - Providing examples in the prompt to help the AI understand the desired output format or style.

**Fine-Tuning** - Customizing a pre-trained AI model with additional training data for specific use cases.

**Fixture** - A fixed, prepared test input or setup that makes a test run the same way every time. A "healthy" fixture is a normal case; a fault fixture contains a known error.

*Svenska:* **förberedd testdata** – Förberedd och oförändrad indata eller miljö som gör att ett test körs likadant varje gång. En "frisk" fixture är ett normalfall, en felfixture innehåller ett känt fel.

## G

**Golden Dataset** - A versioned collection of example inputs with expected or approved answers, used to check whether a change to a prompt, model or retrieval step made results worse. A small set cannot cover every real-world case.

*Svenska:* **referensdataset, facit** – En versionshanterad samling exempelfrågor med förväntade eller godkända svar. Används för att se om en ändring av prompt, modell eller sökning har försämrat resultaten. En liten samling täcker aldrig alla verkliga fall.

**Groundedness** - Whether each claim in an AI answer is supported by the source material the model was given. A groundedness check can hold back unsupported claims, but it does not catch every factual error.

*Svenska:* **förankring i källor** – Om varje påstående i ett AI-svar faktiskt stöds av källmaterialet som modellen fick. En sådan kontroll kan hålla tillbaka påståenden utan stöd, men fångar inte alla faktafel.

**Guardrail** - A rule or check placed around an AI model to block unwanted input or output, such as injection attempts or sensitive data. A guardrail that is described or configured has not necessarily been shown to work.

*Svenska:* **skyddsräcke** – En regel eller kontroll runt en AI-modell som stoppar oönskad indata eller utdata, t.ex. injektionsförsök eller känsliga uppgifter. Att ett skydd finns beskrivet eller inställt betyder inte att det har visats fungera.

## H

**Hallucination** - When an AI generates false or fabricated information that appears plausible.

**Handoff** - The point where one agent, service or person passes a task and its context to another. Handoff tests check that context is not lost and that ownership is clear; a delivered message is not a completed task.

*Svenska:* **överlämning** – När en agent, tjänst eller person lämnar över en uppgift med dess sammanhang till en annan. Tester kontrollerar att inget sammanhang tappas och att det är tydligt vem som äger uppgiften. Ett levererat meddelande är inte en utförd uppgift.

**Human-in-the-Loop (HITL)** - A setup where a person must review or approve certain AI actions, such as writing or changing data, before they take effect.

*Svenska:* **människa i loopen** – En person måste granska eller godkänna vissa AI-handlingar, t.ex. att skriva eller ändra data, innan de genomförs.

## I

**Integration Test** - A test that checks that several components work correctly together, for example an application, its database and a message queue. Passing in a test environment does not prove the same in production.

*Svenska:* **integrationstest** – Kontrollerar att flera delar fungerar ihop, t.ex. en applikation, dess databas och en meddelandekö. Att det fungerar i testmiljön bevisar inte att det fungerar i produktion.

## L

**Least Privilege** - Giving a user, service or agent only the permissions it needs for its task and nothing more, often enforced with an allowlist of permitted actions.

*Svenska:* **minsta möjliga behörighet** – En användare, tjänst eller agent får bara de rättigheter den behöver för sin uppgift, ofta styrt med en lista över tillåtna handlingar (allowlist).

**Linting** - Automatic checking of code for syntax errors, style problems and likely mistakes without running it. Often combined with type checking under the name "static checks". Passing a linter does not prove that the program behaves correctly.

*Svenska:* **automatisk kodkontroll (lintning)** – Automatisk kontroll av kod efter syntaxfel, stilproblem och troliga misstag, utan att koden körs. Kombineras ofta med typkontroll under namnet statiska kontroller. Godkänd lintning bevisar inte att programmet beter sig rätt.

**LLM-as-a-Judge** - Using a language model to score or grade another model's answers. Cheaper "fast judges" can check samples often, while more thorough "deep judges" run less often. A model judge can disagree with qualified human reviewers.

*Svenska:* **AI-modell som bedömare** – En språkmodell används för att poängsätta eller bedöma en annan modells svar. Snabba och billigare bedömare kan köras ofta på stickprov, medan grundligare bedömare körs mer sällan. En AI-bedömare kan göra en annan bedömning än en kunnig människa.

## M

**MCP (Model Context Protocol)** - A standardized protocol for connecting AI models to external tools and data sources.

**Mock** - A simplified stand-in for a real component, such as a fake database or API, used in tests. Mocks make tests fast but can hide real integration problems.

*Svenska:* **låtsaskomponent, attrapp** – En förenklad ersättare för en riktig del, t.ex. en låtsasdatabas eller ett låtsas-API, som används i tester. Gör testerna snabba men kan dölja verkliga problem i samspelet mellan delarna.

**Multi-Agent System** - Multiple AI agents working together, each with specialized roles and capabilities.

## N

**Nightly Run** - A larger, scheduled test run, typically overnight, that covers the full evaluation set instead of a sample. It complements the quick checks run on each commit.

*Svenska:* **nattlig testkörning** – En större schemalagd testkörning, ofta nattetid, som går igenom hela utvärderingssamlingen i stället för ett stickprov. Kompletterar de snabba kontrollerna vid varje commit.

## P

**Prompt** - The input text or instructions given to an AI model.

**Prompt Engineering** - The systematic practice of designing, optimizing, and refining prompts to achieve desired AI outputs.

**Prompt Injection** - A security vulnerability where malicious instructions are hidden within input to manipulate AI behavior.

**Prompt Library** - A centralized collection of tested, optimized prompts for organizational use.

**Pull Request (PR)** - A request to merge a set of code changes into the main code base, where others can review the changes and automated tests run before they are accepted.

*Svenska:* **ändringsförfrågan** – En begäran om att föra in ändringar i huvudkoden, där andra kan granska dem och automatiska tester körs innan de godkänns.

## R

**RAG (Retrieval-Augmented Generation)** - A technique that enhances AI responses by retrieving relevant information from external sources.

**Recall@k** - A search metric: the share of the relevant documents that appear among the top k results. A high score shows that the right material was found, not that the final answer is true.

*Svenska:* **andel relevanta träffar bland de k första** – Ett mått för sökning: hur stor del av de relevanta dokumenten som finns bland de k översta träffarna. Ett högt värde visar att rätt material hittades, inte att det slutliga svaret är sant.

**Red Teaming** - Deliberately attacking your own system, as an adversary would, to find weaknesses. Saved attacks can be re-run as regression tests, but passing them does not prove that the system is secure in general.

*Svenska:* **angreppstester (red teaming)** – Man angriper medvetet sitt eget system som en motståndare skulle göra, för att hitta svagheter. Sparade attacker kan köras igen som regressionstester, men att klara dem bevisar inte att systemet är säkert i allmänhet.

**Regression Test** - A test that is re-run after changes to make sure that something which used to work has not broken. In AI systems this often means re-running the golden dataset after changing a prompt, model or retrieval step.

*Svenska:* **regressionstest** – Ett test som körs om efter ändringar för att se att något som fungerade tidigare inte har gått sönder. I AI-system betyder det ofta att man kör om referensdatasetet efter att ha ändrat prompt, modell eller sökning.

**Retrieval** - The search step in a RAG system that finds passages to give the model before it answers. Retrieval is tested separately from the answer, because weak or irrelevant passages lead to weak answers.

*Svenska:* **hämtning, sökning** – Söksteget i ett RAG-system som letar fram textstycken åt modellen innan den svarar. Testas separat från svaret, eftersom svaga eller irrelevanta träffar ger svaga svar.

**Role Prompting** - Assigning a specific persona or expertise to the AI (e.g., "You are an expert technical writer").

## S

**Sampled Evaluation** - Checking a random selection of test cases instead of all of them, to save time and cost. Sampling gives quick feedback but can miss problems in the cases that were not selected.

*Svenska:* **stickprovsutvärdering** – Man kontrollerar ett slumpmässigt urval av testfallen i stället för alla, för att spara tid och pengar. Ger snabb återkoppling men kan missa problem i de fall som inte kom med.

**Sandbox** - An isolated environment where code or agent actions can be tried without affecting real systems or data.

*Svenska:* **sandlåda, testmiljö** – En avskild miljö där kod eller agenthandlingar kan provas utan att påverka riktiga system eller data.

**Schema** - A formal description of what data must look like: which fields exist, which are required and what type each value has (e.g. JSON Schema).

*Svenska:* **schema, datamall** – En formell beskrivning av hur data ska se ut: vilka fält som finns, vilka som är obligatoriska och vilken typ varje värde ska ha (t.ex. JSON Schema).

**Short-Circuit (Early Exit)** - Stopping a test run as soon as a cheap check fails, so that more expensive checks, such as model-based evaluation, are not run unnecessarily.

*Svenska:* **tidigt avbrott** – En testkörning stoppas så fort en billig kontroll misslyckas, så att dyrare kontroller, t.ex. AI-baserad utvärdering, inte körs i onödan.

**System Prompt** - Instructions that define the AI's behavior across an entire conversation, typically set by the application developer.

## T

**Temperature** - A parameter controlling the randomness/creativity of AI outputs (lower = more deterministic, higher = more creative).

**Test Gate** - A checkpoint in a pipeline that a change or request must pass before it moves on. If the check fails, the change is stopped, retried or sent for review.

*Svenska:* **kontrollpunkt (testgrind)** – En kontrollpunkt i ett flöde som en ändring eller förfrågan måste passera för att gå vidare. Om kontrollen inte går igenom stoppas ändringen, görs om eller skickas till granskning.

**Threat Model** - A structured review of what needs protecting, who might misuse the system and where untrusted data crosses into trusted parts (trust boundaries). It guides which protections to build but enforces nothing by itself.

*Svenska:* **hotmodell** – En genomgång av vad som behöver skyddas, vem som kan missbruka systemet och var opålitlig data passerar in i betrodda delar (förtroendegränser). Den visar vilka skydd som behövs men skyddar ingenting i sig.

**Token** - The basic unit of text processing for AI models. Roughly 4 characters or 3/4 of a word in English.

**Tool Use** - The ability of AI models to call external functions or APIs to accomplish tasks.

**Trace** - A recorded log of the steps a system took for one request, such as which documents were retrieved, which tools were called and what the model answered. Traces from live use are needed to judge quality after release.

*Svenska:* **spårlogg** – En sparad logg över stegen systemet tog för en förfrågan, t.ex. vilka dokument som hämtades, vilka verktyg som anropades och vad modellen svarade. Spår från verklig användning behövs för att bedöma kvaliteten efter lansering.

## U

**Unit Test** - A small, fast test of one piece of code in isolation, such as a single function, including edge cases and error handling.

*Svenska:* **enhetstest** – Ett litet, snabbt test av en enskild koddel, t.ex. en funktion, inklusive gränsfall och felhantering.

**Untrusted Content** - Any text the system did not write itself, such as user input, web pages or retrieved documents. It should be treated as data, never as instructions, because it may contain prompt injection.

*Svenska:* **opålitligt innehåll** – All text som systemet inte själv har skrivit, t.ex. användarinmatning, webbsidor eller hämtade dokument. Ska behandlas som data och aldrig som instruktioner, eftersom den kan innehålla promptinjektion.

## V

**Verification Receipt** - A record of what a check actually examined and what it found, kept as evidence. A statement such as "change completed" is only a claim; the receipt is what lets someone verify it.

*Svenska:* **verifieringskvitto** – En sparad uppgift om vad en kontroll faktiskt undersökte och kom fram till. Ett påstående som "ändringen är klar" är bara ett påstående; kvittot gör att någon kan kontrollera det.

## Z

**Zero-Shot** - Asking an AI to perform a task without providing examples in the prompt.

---

[← Back to Resources](../README.md)
