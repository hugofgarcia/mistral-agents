# mistral-agents

Monorepo dos agentes gerenciados (Mistral Agents SDK). Uma pasta por agente;
cada agente faz o seu próprio deploy a partir da sua pasta.

## product-owner

Fusão do antigo Business Expert e do antigo Product Owner.

- **Moeda:** Concept Document, ELIC-XX, OBJ-XX, BR-XX, GLOSSARIO, FLUX-XX, MVP-TRIAGE, US-XX.
- **Fronteiras:** escreve o Gherkin (definition of tests), nunca código de teste (Tester); nunca REQ-XX/D-XX/ADR-NNNN; nunca implementa.
- **Skills:** anexadas por UUID do registry do Studio (ver main.py), versões pinadas por skill.
- **Conector:** github_escrita_b476 (artifact store hugofgarcia/agent-artifacts).

### Deploy

```bash
cd product-owner
export MISTRAL_API_KEY=<chave>
uv run agents deploy
```

### Teste local

```bash
cd product-owner
uv run agents chat
```

## Convenções

- Artefactos de negócio vivem no repositorio agent-artifacts (projects/<project>/<area>/<ID>.md), nunca nesta repo.
- Skills vivem no registry do Studio; esta repo so guarda codigo de agentes.
- Cada pasta de agente e um workspace uv proprio (lock isolado).
