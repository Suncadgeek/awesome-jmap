# Awesome JMAP [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of JMAP resources, implementations, libraries, tooling, and integrations.
>
> JMAP is a modern JSON-over-HTTP protocol for email, contacts, calendars, and related data. It is designed to replace much of the IMAP + SMTP submission + CardDAV + CalDAV stack with an API that is simpler to implement and faster to sync.

This list focuses on software with native JMAP support, JMAP-focused developer libraries, and practical tooling built on top of JMAP providers such as Fastmail.

## Contents

- [Official Resources](#official-resources)
- [Specifications and Standards](#specifications-and-standards)
- [Providers and Sandboxes](#providers-and-sandboxes)
- [Clients](#clients)
- [Servers](#servers)
- [Libraries and SDKs](#libraries-and-sdks)
- [Tools, Automation, and Plugins](#tools-automation-and-plugins)
- [MCP Servers](#mcp-servers)
- [Proxies and Bridges](#proxies-and-bridges)
- [Deployment](#deployment)
- [Watching](#watching)

## Official Resources

- [JMAP.io](https://jmap.io/) - The main JMAP website with explainers, guides, specs, news, and implementation listings.
- [JMAP Specifications](https://jmap.io/spec.html) - Index of the current RFCs, extensions, and in-progress work.
- [Client Developer Guide](https://jmap.io/client.html) - Recommended starting point for client authors.
- [Server Implementation Guide](https://jmap.io/server.html) - Practical guidance for server implementers.
- [Software Implementations](https://jmap.io/software.html) - The canonical public list of JMAP-aware clients, servers, libraries, and requested integrations.
- [JMAP Working Group](https://datatracker.ietf.org/wg/jmap/about/) - IETF working group for the protocol and its extensions.
- [jmapio/jmap](https://github.com/jmapio/jmap) - Source repository for the JMAP specifications and supporting documentation.

## Specifications and Standards

### Core

- [RFC 8620: JMAP Core](https://www.rfc-editor.org/rfc/rfc8620) - Core protocol, capabilities, session discovery, and object model.
- [RFC 8887: JMAP over WebSocket](https://www.rfc-editor.org/rfc/rfc8887) - WebSocket transport for low-latency clients.
- [RFC 9404: JMAP Blob Management](https://www.rfc-editor.org/rfc/rfc9404) - Managing binary data and uploaded blobs.
- [RFC 9425: JMAP Quotas](https://www.rfc-editor.org/rfc/rfc9425) - Standard quota capability.
- [RFC 9670: JMAP Sharing](https://www.rfc-editor.org/rfc/rfc9670) - Shared mail, contacts, calendars, and access rights.
- [RFC 9749: VAPID for JMAP Push](https://www.rfc-editor.org/rfc/rfc9749) - Push security for JMAP mobile/web notification flows.

### Mail

- [RFC 8621: JMAP Mail](https://www.rfc-editor.org/rfc/rfc8621) - Email objects, mailboxes, submission, and search.
- [RFC 9007: JMAP MDN Handling](https://www.rfc-editor.org/rfc/rfc9007) - Read receipts and message disposition notifications.
- [RFC 9219: JMAP S/MIME Signature Verification](https://www.rfc-editor.org/rfc/rfc9219) - S/MIME verification metadata for clients.
- [RFC 9661: JMAP Sieve Scripts Management](https://www.rfc-editor.org/rfc/rfc9661) - Managing Sieve scripts through JMAP.

### Contacts and Calendars

- [RFC 9610: JMAP Contacts](https://www.rfc-editor.org/rfc/rfc9610) - Contacts data modeled with JSContact.
- [JMAP Calendars Draft](https://www.ietf.org/archive/id/draft-ietf-jmap-calendars-latest.html) - Current in-progress calendaring spec.
- [RFC 9553: JSContact](https://www.rfc-editor.org/rfc/rfc9553) - JSON contact format used by JMAP Contacts.
- [JSCalendar 2.0 Draft](https://www.ietf.org/archive/id/draft-ietf-calext-jscalendar-latest.html) - JSON calendar format used by JMAP Calendars work.

## Providers and Sandboxes

- [Fastmail](https://www.fastmail.com/) - The best-known public JMAP provider and the source of much of the surrounding ecosystem.
- [Topicbox](https://www.topicbox.com/) - Hosted group-email product listed by JMAP as a public place to try the protocol.
- [JMAP Demo Webmail](https://github.com/jmapio/jmap-demo-webmail) - Reference webmail client that doubles as a useful test target and learning resource.
- [Demo Fastmail API JMAP](https://github.com/joelparkerhenderson/demo-fastmail-api-jmap) - Small demo project for experimenting with Fastmail's JMAP API.
- [JMAP Samples](https://github.com/fastmail/JMAP-Samples) - Official sample code from Fastmail for developers getting started with JMAP.

## Clients

- [aerc](https://aerc-mail.org/) - Terminal email client with JMAP support.
- [Bulwark Webmail](https://bulwarkmail.org/) - Modern JMAP-native webmail for Stalwart with mail, calendar, contacts, and files.
- [Cypht](https://github.com/cypht-org/cypht) - Lightweight open source webmail aggregator with JMAP support.
- [Group-Office](https://github.com/Intermesh/groupoffice) - Open source groupware platform with JMAP support.
- [JMAP Webmail](https://github.com/root-fr/jmap-webmail) - Privacy-focused webmail client with real-time push support.
- [Ltt.rs](https://codeberg.org/iNPUTmice/lttrs-android) - Android email client.
- [Mailtemi](https://mailtemi.com/) - Native mobile and desktop mail client with JMAP support.
- [meli](https://meli.delivery/) - Terminal mail client written in Rust.
- [Parula](https://parula.beonex.com/) - Cross-platform email app with chat, conferencing, and calendar support.
- [Plume](https://plume.kler.dev/) - Native iOS and macOS email client with a privacy focus.
- [ratatoskr](https://github.com/folknor/ratatoskr) - Rust desktop email client with JMAP, IMAP, Gmail, and Exchange/Graph support.
- [Twake Mail Client](https://github.com/linagora/tmail-flutter) - Flutter-based JMAP client for Android, iOS, and the web.
- [Kolumba](https://github.com/satriadhikara/kolumba) - Webmail client purpose-built for Stalwart Mail Server with native JMAP.
- [Leithmail](https://github.com/leithmail/leithmail) - Cross-platform JMAP email client for web, Android, and iOS built with Dart/Flutter.

## Servers

- [Apache James](https://james.apache.org/) - Java mail server project adding and extending JMAP support.
- [atmail](https://www.atmail.com/blog/jmap-rfc-8620/) - Commercial mail platform with JMAP support.
- [Cyrus IMAP](https://www.cyrusimap.org/) - Mature IMAP server with JMAP support and implementation docs.
- [Group-Office](https://www.group-office.com/) - Groupware platform that can also act as a JMAP-capable backend.
- [Stalwart Mail Server](https://github.com/stalwartlabs/stalwart) - Full mail and collaboration server with broad JMAP coverage, including contacts, calendars, storage, and sharing.
- [Twake Mail Backend](https://github.com/linagora/tmail-backend) - JMAP-capable backend built on Apache James.

## Libraries and SDKs

### Go

- [go-jmap](https://sr.ht/~rockorager/go-jmap) - JMAP client library written in Go.
- [jmap-service-email](https://github.com/jarrod-lowe/jmap-service-email) - Serverless JMAP email service on AWS Lambda backed by DynamoDB and S3.

### Java and JVM

- [Java JMAP Library](https://codeberg.org/iNPUTmice/jmap/) - Low-level JMAP client plus higher-level mail-user-agent building blocks.
- [jmap-examples](https://github.com/iNPUTmice/jmap-examples) - JMAP code examples in Java from the iNPUTmice team.

### JavaScript and TypeScript

- [JMAP-JS](https://github.com/jmapio/jmap-js) - Full JavaScript implementation of JMAP mail, calendar, and contacts models.
- [jmap-client-ts](https://github.com/OpenPaaS-Suite/jmap-client-ts) - Lightweight promise-based TypeScript client.
- [jmap-jam](https://github.com/htunnicliff/jmap-jam) - Tiny strongly typed TypeScript client with fluent APIs.
- [jmap-kit](https://github.com/lachlanhunt/jmap-kit) - Type-safe TypeScript SDK with plugin support for standard and vendor capabilities.
- [jmap-yacl](https://github.com/ilyhalight/jmap-yacl) - Lightweight client library for JavaScript and TypeScript projects.

### Python

- [jmapc](https://github.com/smkent/jmapc) - Python 3 JMAP client library.
- [python-jmap](https://github.com/boopmail/python-jmap) - Idiomatic Python library for working with JMAP.

### Rust

- [calcard](https://github.com/stalwartlabs/calcard) - JSCalendar/iCalendar and JSContact/vCard parsing and conversion library.
- [io-jmap](https://github.com/pimalaya/io-jmap) - I/O-free JMAP client library written in Rust.
- [jmap-client](https://github.com/stalwartlabs/jmap-client) - Rust JMAP client library with core, mail, and WebSocket support.
- [jmap-rs](https://gitlab.com/jmap-rs/jmap-rs) - In-progress Rust client library.
- [jmap-tools](https://github.com/stalwartlabs/jmap-tools) - JMAP object parser with JSON Pointer querying and patch support.
- [melib](https://github.com/meli/meli) - Mail library used by `meli`, including JMAP support.
- [Missive](https://github.com/jeffhuen/missive) - Email library with a JMAP provider and a minimal spec-compliant client.

### .NET

- [JMAP.Net](https://github.com/JMAP-Net/JMAP.Net) - Modern .NET implementation of the core JMAP mail protocol.
- [JSCalendar.Net](https://github.com/JMAP-Net/JSCalendar.Net) - .NET support library for the JSCalendar data model used by JMAP calendars work.

### PHP

- [zend-jmap](https://github.com/WikiSuite/zend-jmap) - JMAP support for Zend Framework.

### Swift

- [swift-jmap-client](https://github.com/kukushechkin/swift-jmap-client) - JMAP client library for Swift/iOS/macOS.

### Nim

- [jmap-client](https://github.com/aryonoco/jmap-client) - JMAP client library written in Nim.

## Tools, Automation, and Plugins

### General Tools

- [JMAP-Tester](https://github.com/fastmail/JMAP-Tester) - Perl client designed for writing tests against JMAP servers.
- [JMAP-TestSuite](https://github.com/fastmail/JMAP-TestSuite) - Protocol test suite for validating JMAP implementations.
- [jmap-backup](https://github.com/luckman212/jmap-backup) - Backup a Fastmail JMAP mailbox to `.eml` files.
- [jmap-blog](https://github.com/YohannParis/jmap-blog) - Publish a blog from a JMAP mailbox.
- [mjmap](https://git.sr.ht/~rockorager/mjmap) - Sendmail-compatible command line JMAP client.
- [mujmap](https://github.com/elizagamedev/mujmap) - Synchronize JMAP mail with `notmuch`.
- [n8n-nodes-jmap](https://github.com/mmaudet/n8n-nodes-jmap) - Community n8n node for JMAP email workflows and agent integrations.
- [waffles](https://github.com/smkent/waffles) - Auto-reply bot for JMAP mailboxes.

### CLI Tools

- [jmap-cli](https://github.com/audriga/jmap-cli) - Command line client for JMAP servers, written in Dart.
- [fastmail-cli](https://github.com/radiosilence/fastmail-cli) - CLI for querying Fastmail's JMAP API with structured JSON output for AI integration.
- [fm](https://github.com/zacharytamas/fm) - Fastmail JMAP CLI for triaging mailboxes and messages.
- [FastMask](https://github.com/pawelorzech/FastMask) - Android app for managing Fastmail masked emails via JMAP.

### Fastmail-Focused

- [fastmail-mcp-server](https://github.com/keineantwort/fastmail-mcp-server) - MCP server for Fastmail email search, reading, and summarization via JMAP.
- [mailboxzero](https://github.com/taskinen/mailboxzero) - Clean up a Fastmail inbox by finding and archiving similar mail through JMAP.
- [mailroom](https://github.com/HelloThisIsFlo/mailroom) - Pluggable email workflow automation for Fastmail using JMAP, CardDAV, and label-based triage.
- [pyfastmail-mcp](https://github.com/pjosols/pyfastmail-mcp) - Python MCP server for Fastmail email, calendars, contacts, and files over JMAP.

## MCP Servers

MCP (Model Context Protocol) servers expose JMAP email operations to AI assistants and coding agents.

- [jmap-mcp](https://github.com/wyattjoh/jmap-mcp) - MCP server providing tools for interacting with JMAP email servers.
- [jmap-mcp-rs](https://github.com/arlyon/jmap-mcp-rs) - MCP server for JMAP written in Rust.
- [jmap-mcp](https://github.com/mikluko/jmap-mcp) - MCP server for JMAP written in Go.
- [jmap-mcp-server](https://github.com/willmeyers/jmap-mcp-server) - Stable MCP server for JMAP servers like Fastmail, written in Python.
- [fastmail-mcp](https://github.com/erict-dev/fastmail-mcp) - MCP server for JMAP, built for Fastmail but compatible with any JMAP-capable server.
- [mcp-server-stalwart](https://github.com/codeChap/mcp-server-stalwart) - MCP server for Stalwart mail server via JMAP, written in Rust.
- [mailbox-mcp](https://github.com/jgalea/mailbox-mcp) - Multi-provider email MCP server with Gmail, IMAP, and JMAP support.
- [mcp-twake-mail](https://github.com/mmaudet/mcp-twake-mail) - MCP server for JMAP email operations with Twake Mail.
- [officemail](https://github.com/nextintelligence-ai/officemail-official) - Officemail plugin for Claude Code for email management via JMAP.

### Stalwart and CMS Integrations

- [OpenClaw Stalwart JMAP Plugin](https://github.com/pew/openclaw-stalwart-jmap-plugin) - Connect Stalwart JMAP data to AI agent workflows.
- [WordPress JMAP](https://github.com/bulwarkmail/wordpress-jmap) - WordPress integration built around JMAP workflows.

## Proxies and Bridges

- [hyper-auth-proxy](https://crates.io/crates/hyper-auth-proxy) - Proxy that adds JWT bearer auth in front of Cyrus JMAP.
- [IMAP-to-JMAP Proxy](https://github.com/stalwartlabs/imap-to-jmap) - Open source IMAP4-to-JMAP proxy.
- [JMAP-to-IMAP Proxy](https://github.com/jmapio/jmap-perl) - JMAP server implementation backed by existing IMAP, CalDAV, and CardDAV stores.
- [mailjail](https://github.com/akaihola/mailjail) - JMAP-IMAP proxy with restricted access, written in Python.
- [roundcube-jmap](https://github.com/audriga/roundcube-jmap) - JMAP API plugin for Roundcube Webmail.

## Deployment

- [keycloak-stalwart-stack](https://github.com/Souheib-h/keycloak-stalwart-stack) - Keycloak IAM + Stalwart Mail Server + JMAP Webmail, Docker-tested and Proxmox-deployed.
- [cyrus-jmap-docker](https://github.com/remk/cyrus-jmap-docker) - Cyrus Docker image with JMAP support.

## Watching

### Planned

- [Mimestream](https://mimestream.com/) - Native macOS client listed by JMAP as planned.

### Requested Support

- [Alps Webmail](https://todo.sr.ht/~migadu/alps/174) - Open request for JMAP support.
- [Claws Mail](https://www.thewildbeast.co.uk/claws-mail/bugzilla/show_bug.cgi?id=4057) - Open request for JMAP support.
- [DavMail](https://github.com/mguessan/davmail/issues/365) - Open request for JMAP support.
- [Evolution](https://gitlab.gnome.org/GNOME/evolution/-/issues/364) - Open request for JMAP support.
- [Geary](https://gitlab.gnome.org/GNOME/geary/-/issues/327) - Open request for JMAP support.
- [Horde IMP Webmail](https://bugs.horde.org/ticket/14683) - Open request for JMAP support.
- [K-9 Mail](https://github.com/k9mail/k-9/issues/3272) - Open request for JMAP support.
- [Mailu](https://github.com/Mailu/Mailu/issues/471) - Open request for JMAP support.
- [Nextcloud Mail](https://github.com/nextcloud/mail/issues/2931) - Open request for JMAP support.
- [RainLoop](https://github.com/RainLoop/rainloop-webmail/issues/1378) - Open request for JMAP support.
- [SnappyMail](https://github.com/the-djmaze/snappymail/issues/1550) - Open request for JMAP support.
- [Thunderbird](https://bugzilla.mozilla.org/show_bug.cgi?id=1322991) - Long-running JMAP support request.

## Contributing

Pull requests are welcome.

When adding an entry, prefer projects that are:

- JMAP-native clients, servers, libraries, or bridges
- Official specifications, implementation guides, or public provider docs
- Practical tooling that directly uses JMAP for backup, testing, automation, or integrations

If a project only has an issue asking for JMAP support, add it to the `Watching` section instead of the main sections.
