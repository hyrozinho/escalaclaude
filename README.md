# /escala — Escala

Skill pro [Claude Code](https://claude.ai/claude-code) que transforma operacao de low ticket digital num software interativo. Mineracao de ofertas escaladas, modelagem de funil, geracao de criativos, cadastro em gateway e otimizacao de campanhas — tudo dentro do terminal.

**by [@ogestorsantiago_](https://instagram.com/ogestorsantiago_)**

## O que faz

| Modulo | Descricao |
|--------|-----------|
| [1] Setup | Diagnostico de dependencias |
| [2] Minerar | Reclame Aqui, Biblioteca Meta, RatoAds |
| [3] Analisar | Analise completa de oferta + definir produto |
| [4] Entregavel | Gera PDF/pack/planilha/simulado completo |
| [5] Funil | Modela pagina de vendas a partir do concorrente |
| [6] Criativos | Scrapa ads reais, transcreve, gera 7 criativos modelados |
| [7] Gateway | Cadastra produto na Wiapy automaticamente |
| [8] Meta Ads | Cria pixel, campanha e otimiza (metodo @ogestorsantiago_) |
| [9] Config | Diagnostico, instalacao, metricas |

## Como instalar (passo a passo)

1. Tenha o Claude Code instalado no seu computador.

2. No terminal, clone o repositorio da skill:

```bash
git clone https://github.com/hyrozinho/gatee.git
```

3. Copie a skill para a pasta de skills do Claude Code:

```bash
cp -r gatee ~/.claude/skills/escala
```

4. Entre na pasta da skill:

```bash
cd gatee
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

O `minerador-reclameaqui.py` scrapa reclamacoes de 8 gateways pra encontrar ofertas escaladas.

```bash
# Todos os 8 gateways
python minerador-reclameaqui.py

# Gateways especificos
python minerador-reclameaqui.py wiapy,cakto,kirvano 10 15
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
