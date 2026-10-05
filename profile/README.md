## Attricat

Attricat is a catalog for structured product and reference data whose shape changes over time.

You describe each kind of record with a blueprint. Publishing a blueprint freezes it as a revision, and every entity stays on the revision it was created with until someone migrates it. Values that differ by market, language, or channel live in contexts and inherit down a tree, so you set them once and override only where needed. Publishing approves an entity for a channel, and any later edit withdraws that approval.

People, integrations, and AI agents all change data through the same path. The server validates each change, writes it to the audit log, and keeps it in history. Agents can draft edits, but a person approves them before they are saved.

- Website: [attricat.com](https://attricat.com)
- Docs: [docs.attricat.com](https://docs.attricat.com) (English and Polish)

### Repositories

| Repository | What it is |
| --- | --- |
| [attricat](https://github.com/attricat/attricat) | The core: Rust (Axum) API, `acli` command-line client, and React web app. AGPL-3.0. |
| [attricat-extension-example](https://github.com/attricat/attricat-extension-example) | Reference extension. Adds computed numeric attributes and uses most of the extension system along the way. |
| [attricat-connector-csv](https://github.com/attricat/attricat-connector-csv) | CSV import and export connector, run as blueprint connector jobs. |
| [attricat-extensions](https://github.com/attricat/attricat-extensions) | Registry of published extensions. MIT. |

### Where to start

- **Try it:** [Quickstart](https://docs.attricat.com/start/quickstart/) and [Core concepts](https://docs.attricat.com/start/concepts/)
- **Model your data:** [Author a blueprint](https://docs.attricat.com/builders/blueprints/) and the [Blueprint TOML reference](https://docs.attricat.com/reference/blueprint/)
- **Extend it:** [Build an extension](https://docs.attricat.com/extensions/build/). Extensions are WebAssembly components with sandboxed UI, and they can only do what an administrator grants them.
- **Run it:** [Deploy Attricat](https://docs.attricat.com/operate/deployment/) and the [Configuration reference](https://docs.attricat.com/reference/configuration/)

Open bugs and feature requests as issues on the repository they concern. To run the core locally, follow the [attricat README](https://github.com/attricat/attricat#run-it-locally).
