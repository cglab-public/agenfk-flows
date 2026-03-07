# AgEnFK Flows

A public repository of community-contributed **Flows** for [AgEnFK](https://github.com/cglab-public/agenfk) — the Agentic Engineering Framework.

## What is a Flow?

In AgEnFK, a **Flow** defines the workflow lifecycle for your project's tasks. Instead of the default statuses (`TODO → IN_PROGRESS → REVIEW → DONE`), you can design a custom sequence of steps — each with its own name and exit criteria — that matches how your team actually works.

Examples:
- **TDD Flow**: `TODO → create_unit_tests → IN_PROGRESS → REVIEW → DONE`
- **Design-First Flow**: `TODO → design → implementation → qa → DONE`
- **Hotfix Flow**: `TODO → fix → verify → DONE`

## Using a Flow

1. Browse the flows in this repository.
2. Copy the flow JSON into your AgEnFK project settings, or use the Flow Editor in the dashboard.
3. The flow becomes your workflow contract — each step's exit criteria guides your agent before it can advance.

## Contributing a Flow

Contributions are welcome! To share a flow with the community:

1. Fork this repository.
2. Add your flow as a `.json` file under a descriptive directory (e.g. `tdd/tdd-flow.json`).
3. Include a short `README.md` in the same directory explaining the flow's purpose and intended use case.
4. Open a pull request.

### Flow file format

```json
{
  "name": "My Flow",
  "steps": [
    {
      "name": "design",
      "exitCriteria": "Design document reviewed and approved."
    },
    {
      "name": "implementation",
      "exitCriteria": "All acceptance criteria implemented and unit tests passing."
    },
    {
      "name": "qa",
      "exitCriteria": "QA sign-off received; no open blockers."
    }
  ]
}
```

> **Note:** The first and last steps are anchors (`TODO` and `DONE`) added automatically by AgEnFK. Only define the intermediate steps.

## License

Flows in this repository are shared under the [MIT License](LICENSE) unless otherwise noted.
