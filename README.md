# /escala — Escala

Skill pro [Claude Code](https://claude.ai/claude-code) que transforma operacao de low ticket digital num software interativo. Mineracao de ofertas escaladas, modelagem de funil, geracao de criativos e otimizacao de campanhas — tudo dentro do terminal.

**by [@yuri.mkt7](https://instagram.com/yuri.mkt7) e [@miguelmkt8](https://instagram.com/miguelmkt8)**

## O que faz

| Modulo | Descricao |
|--------|-----------|
| [1] Setup | Diagnostico de dependencias |
| [2] Minerar | Reclame Aqui e Biblioteca Meta |
| [3] Analisar | Analise completa de oferta + definir produto |
| [4] Entregavel | Gera PDF/pack/planilha/simulado completo |
| [5] Funil | Modela pagina de vendas a partir do concorrente |
| [6] Criativos | Scrapa ads reais, transcreve, gera 7 criativos modelados |
| [7] Meta Ads | Cria pixel, campanha e otimiza (metodo @yuri.mkt7 e @miguelmkt8) |
| [8] Config | Diagnostico, instalacao, metricas |

## Como instalar (passo a passo)

1. Tenha o Claude Code instalado no seu computador.

2. No terminal, clone o repositorio da skill:

```bash
git clone https://github.com/hyrozinho/escalaclaude.git
```

3. Copie a skill para a pasta de skills do Claude Code:

```bash
cp -r escalaclaude ~/.claude/skills/escala
```

4. Entre na pasta da skill:

```bash
cd escalaclaude
```

5. Crie seu arquivo de configuracao:

```bash
cp config-escala.example.json config-escala.json
```

6. Abra o Claude Code e rode o comando da skill:

```text
/escala
```

7. Dentro da skill, rode `[1] Setup` para fazer a configuracao inicial.

## Minerador Reclame Aqui

O `minerador-reclameaqui.py` scrapa reclamacoes em gateways de pagamento pra encontrar ofertas escaladas.

```bash
# Todos os gateways suportados
python minerador-reclameaqui.py

# Gateways especificos
python minerador-reclameaqui.py cakto,kirvano 10 15
```

Requer Edge instalado. Resultados salvos em `./mineracao/`.

## Estrutura de pastas (geradas automaticamente)

```
./mineracao/          resultados do Reclame Aqui
./analises/           analises de ofertas salvas
./produtos/           definicoes de produto
./entregaveis/        PDFs, packs, planilhas gerados
./funis/              paginas de vendas HTML
./criativos/          roteiros, vozes, videos de fundo
```

## Licenca

MIT
