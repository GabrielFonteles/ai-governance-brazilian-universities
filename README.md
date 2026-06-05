# projeto_template

Template base para projetos de pesquisa em humanidades digitais.

## Como usar este template

1. Acesse github.com/GabrielFonteles/projeto_template
2. Clique em **Use this template** → **Create a new repository**
3. Dê um nome ao repositório e clique em **Create repository**
4. Clone para a máquina:

```bash
git clone https://github.com/GabrielFonteles/nome_do_projeto ~/projetos/nome_do_projeto
```

5. Entre na pasta e crie o ambiente virtual:

```bash
cd ~/projetos/nome_do_projeto
uv venv
source .venv/bin/activate
```

6. Instale as dependências:

```bash
uv pip install -r requirements.txt
```

7. Copie o `.env.example` para `.env` e preencha com suas chaves:

```bash
cp .env.example .env
```

8. Atualize o `config.yaml` com o nome e descrição do projeto.

---

## Estrutura de pastas

```
projeto/
├── dados/
│   ├── brutos/        # Arquivos originais — somente leitura, não versionados
│   └── processados/   # Saídas intermediárias dos scripts
├── notebooks/         # Jupyter notebooks
├── scripts/           # Scripts Python reutilizáveis
├── outputs/           # Resultados finais (CSV, GeoJSON, gráficos)
├── .env               # Chaves de API — nunca versionar
├── .env.example       # Modelo do .env — versionar
├── .gitignore
├── .python-version
├── config.yaml        # Parâmetros centrais do projeto
├── requirements.txt   # Dependências Python
├── README.md
└── RESEARCH_LOG.md    # Log metodológico
```

**Regra fundamental:** a pasta `dados/brutos/` é somente leitura. Nenhum script deve sobrescrever os arquivos originais.

---

## Antes de cada commit

- [ ] `.env` está no `.gitignore` e fora do repositório
- [ ] Nenhuma chave de API no código
- [ ] Outputs dos notebooks limpos
- [ ] RESEARCH_LOG atualizado com decisões metodológicas relevantes

---

## Autor

Gabriel Fonteles
