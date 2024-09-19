# **Next.js AI Chatbot**

<a href="https://chat.vercel.ai/">
  <img alt="Next.js 14 and App Router-ready AI chatbot." src="https://chat.vercel.ai/opengraph-image.png">
  <h1 align="center">Next.js AI Chatbot</h1>
</a>

<p align="center">
  Eine Open-Source AI-Chatbot-App-Vorlage, erstellt mit Next.js, dem Vercel AI SDK, OpenAI und Vercel KV.
</p>

<p align="center">
  <a href="#features"><strong>Funktionen</strong></a> ·
  <a href="#model-providers"><strong>Modell-Anbieter</strong></a> ·
  <a href="#deploy-your-own"><strong>Deine eigene Instanz bereitstellen</strong></a> ·
  <a href="#running-locally"><strong>Lokal ausführen</strong></a> ·
  <a href="#authors"><strong>Autoren</strong></a>
</p>
<br/>

## Funktionen

- [Next.js](https://nextjs.org) App Router
- React Server Components (RSCs), Suspense und Server Actions
- [Vercel AI SDK](https://sdk.vercel.ai/docs) für eine Streaming-Chat-Benutzeroberfläche
- Unterstützung für OpenAI (Standard), Anthropic, Cohere, Hugging Face oder benutzerdefinierte AI-Chat-Modelle und/oder LangChain
- [shadcn/ui](https://ui.shadcn.com)
  - Stilierung mit [Tailwind CSS](https://tailwindcss.com)
  - [Radix UI](https://radix-ui.com) für headless Komponentenelemente
  - Icons von [Phosphor Icons](https://phosphoricons.com)
- Chatverlauf, Rate-Limiting und Sitzungs-Speicherung mit [Vercel KV](https://vercel.com/storage/kv)
- [NextAuth.js](https://github.com/nextauthjs/next-auth) zur Authentifizierung

## Modell-Anbieter

Diese Vorlage wird standardmäßig mit OpenAI `gpt-3.5-turbo` ausgeliefert. Dank des [Vercel AI SDK](https://sdk.vercel.ai/docs) kannst du jedoch die LLM-Anbieter zu [Anthropic](https://anthropic.com), [Cohere](https://cohere.com/), [Hugging Face](https://huggingface.co) oder [LangChain](https://js.langchain.com) mit nur wenigen Codezeilen ändern.

## Deine eigene Instanz bereitstellen

Du kannst deine eigene Version des Next.js AI-Chatbots mit einem Klick auf Vercel bereitstellen:

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?demo-title=Next.js+Chat&demo-description=A+full-featured%2C+hackable+Next.js+AI+chatbot+built+by+Vercel+Labs&demo-url=https%3A%2F%2Fchat.vercel.ai%2F&demo-image=%2F%2Fimages.ctfassets.net%2Fe5382hct74si%2F4aVPvWuTmBvzM5cEdRdqeW%2F4234f9baf160f68ffb385a43c3527645%2FCleanShot_2023-06-16_at_17.09.21.png&project-name=Next.js+Chat&repository-name=nextjs-chat&repository-url=https%3A%2F%2Fgithub.com%2Fvercel-labs%2Fai-chatbot&from=templates&skippable-integrations=1&env=OPENAI_API_KEY%2CAUTH_SECRET&envDescription=How+to+get+these+env+vars&envLink=https%3A%2F%2Fgithub.com%2Fvercel-labs%2Fai-chatbot%2Fblob%2Fmain%2F.env.example&teamCreateStatus=hidden&stores=[{"type":"kv"}])

## Erstellen einer KV-Datenbankinstanz

Folge den Schritten im [Schnellstart-Leitfaden](https://vercel.com/docs/storage/vercel-kv/quickstart#create-a-kv-database) von Vercel, um eine KV-Datenbank auf Vercel zu erstellen und zu konfigurieren, damit deine Anwendung damit interagieren kann.

Vergiss nicht, deine Umgebungsvariablen (`KV_URL`, `KV_REST_API_URL`, `KV_REST_API_TOKEN`, `KV_REST_API_READ_ONLY_TOKEN`) in der `.env`-Datei mit den entsprechenden Anmeldedaten zu aktualisieren, die während des Setups der KV-Datenbank bereitgestellt wurden.

## Lokal ausführen

Um den Next.js AI-Chatbot lokal auszuführen, benötigst du die Umgebungsvariablen, die in der [`.env.example`](.env.example)-Datei definiert sind. Es wird empfohlen, [Vercel Environment Variables](https://vercel.com/docs/projects/environment-variables) zu verwenden, aber eine `.env`-Datei reicht ebenfalls aus.

> Hinweis: Du solltest deine `.env`-Datei nicht committen, da dies Geheimnisse enthält, die es anderen ermöglichen würden, auf deine OpenAI- und Authentifizierungsanbieter-Konten zuzugreifen.

1. Vercel CLI installieren: `npm i -g vercel`
2. Lokale Instanz mit Vercel- und GitHub-Konten verknüpfen (erstellt ein `.vercel`-Verzeichnis): `vercel link`
3. Lade deine Umgebungsvariablen herunter: `vercel env pull`

```bash
pnpm install
pnpm dev
```

Deine App-Vorlage sollte jetzt unter [localhost:3000](http://localhost:3000/) laufen.

## Autoren

Diese Bibliothek wurde von [Vercel](https://vercel.com) und Mitgliedern des [Next.js](https://nextjs.org) Teams erstellt, mit Beiträgen von:

- Jared Palmer ([@jaredpalmer](https://twitter.com/jaredpalmer)) - [Vercel](https://vercel.com)
- Shu Ding ([@shuding\_](https://twitter.com/shuding_)) - [Vercel](https://vercel.com)
- shadcn ([@shadcn](https://twitter.com/shadcn)) - [Vercel](https://vercel.com)
