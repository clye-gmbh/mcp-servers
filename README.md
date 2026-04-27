# mcp-servers

Registry of MCP Servers available in AI Hub.

## Available Servers

### AI Hub CLI

All servers below are part of the [AI Hub CLI](https://github.com/clye-gmbh/ai-hub-cli) — a single binary that exposes multiple MCP servers as subcommands. Install it via:

```sh
curl -fsSL https://ai-hub-cli.s3.de.io.cloud.ovh.net/install.sh | sh
```

or

```sh
go install github.com/clye-gmbh/ai-hub-cli@latest
```

---

#### Executors

| Server | Description | Docs |
|--------|-------------|------|
| **Python Executor** | Sandboxierter Python-Executor mit persistentem Zustand. Führt Python-Code aus und unterstützt optionale UV-basierte venvs sowie Dateiausgaben. Tool: `execute_python`. | [Docs](https://ai-hub-cli.s3.de.io.cloud.ovh.net/index.html#python-executor) |
| **Terminal Executor** | MCP-Server zur Ausführung von Terminal-Befehlen als Vordergrund- oder Hintergrundprozesse mit optionalem Arbeitsverzeichnis. Tool: `execute_terminal`. | [Docs](https://ai-hub-cli.s3.de.io.cloud.ovh.net/index.html#terminal-executor) |
| **Combined Executor** | Kombinierter MCP-Server, der sowohl Python- als auch Terminal-Ausführung in einem einzigen Server bereitstellt. Entspricht dem Standard-Verhalten des Docker-Images. | [Docs](https://ai-hub-cli.s3.de.io.cloud.ovh.net/index.html#combined-executor) |

#### Agent Bridge

| Server | Description | Docs |
|--------|-------------|------|
| **ACP Connector** | Brückt das Agent Client Protocol (ACP) zu lokalen Agenten-Prozessen über stdio. Agenten-Profile werden per JSON-Konfiguration definiert. | [Docs](https://ai-hub-cli.s3.de.io.cloud.ovh.net/index.html#acp-connector) |

#### Database Connectors

Each database connector exposes a single `execute_sql` tool.

| Server | Description | Docs |
|--------|-------------|------|
| **SQLite Connector** | SQLite-Datenbankverbindung. Unterstützt Datei- und In-Memory-Datenbanken. | [Docs](https://ai-hub-cli.s3.de.io.cloud.ovh.net/index.html#sqlite) |
| **PostgreSQL Connector** | Verbindet einen PostgreSQL-Server via Flags, Umgebungsvariablen oder DSN. | [Docs](https://ai-hub-cli.s3.de.io.cloud.ovh.net/index.html#postgresql) |
| **MySQL Connector** | Verbindet einen MySQL-Server via Flags, Umgebungsvariablen oder DSN. | [Docs](https://ai-hub-cli.s3.de.io.cloud.ovh.net/index.html#mysql) |
| **MS SQL Server Connector** | Verbindet einen Microsoft SQL Server via Flags, Umgebungsvariablen oder DSN. | [Docs](https://ai-hub-cli.s3.de.io.cloud.ovh.net/index.html#ms-sql-server) |
| **ClickHouse Connector** | Verbindet einen ClickHouse-Server via Flags, Umgebungsvariablen oder DSN. | [Docs](https://ai-hub-cli.s3.de.io.cloud.ovh.net/index.html#clickhouse) |
| **Oracle Connector** | Verbindet einen Oracle-Datenbankserver (erfordert Oracle Instant Client). Unterstützt SERVICE_NAME und SID. | [Docs](https://ai-hub-cli.s3.de.io.cloud.ovh.net/index.html#oracle) |

#### API & Filesystem

| Server | Description | Docs |
|--------|-------------|------|
| **REST Connector** | Wandelt OpenAPI 3.0 Spezifikationen (JSON oder YAML) in MCP-Tools um. Jede Operation wird zu einem aufrufbaren Tool. Unterstützt Bearer-Token- und Custom-Header-Authentifizierung. | [Docs](https://ai-hub-cli.s3.de.io.cloud.ovh.net/index.html#rest-connector) |
| **Filesystem Connector** | Stellt einen oder mehrere Ordner als MCP-Ressourcen (`filesystem://`) bereit. Unterstützt lesen, schreiben, suchen, verschieben, kopieren und löschen innerhalb konfigurierter Wurzelpfade. | [Docs](https://ai-hub-cli.s3.de.io.cloud.ovh.net/index.html#filesystem-connector) |

---

### Other Servers

| Server | Description | Docs |
|--------|-------------|------|
| **Docs** | Macht die Dokumentation für KI-Assistenten direkt durchsuchbar. | [Docs](https://docs.clye.ai/clye-docs-mcp-server/) |
| **Microsoft 365** | Ermöglicht den Zugriff auf Microsoft 365-Dienste wie E-Mails, Kalender, Dateien, Teams, SharePoint. | [Docs](https://docs.clye.ai/mcp-server-ms-365) |