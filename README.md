# Site — Roteiro Psiquiátrico

Pasta publicada no GitHub Pages. **Todos os arquivos aqui são gerados** — não edite à mão.

| Arquivo | Gerado por |
|---|---|
| `index.html` | `build/build_landing.py` |
| `privacidade.html`, `termos.html` | `build/build_legal.py` (a partir de `docs/legal/*.md`) |
| `amostra.pdf` | cópia de `dist/amostra_gratuita.pdf` (`build/build_sample.js`) |

Para regerar, a partir da raiz do projeto:

```
python build/build_landing.py
python build/build_legal.py
cp dist/amostra_gratuita.pdf site/amostra.pdf
```

## Estado atual: PRIVADO (noindex)

O site está com `<meta name="robots" content="noindex,nofollow">` e `robots.txt` bloqueando tudo.
Ele **não deve sair do noindex** enquanto estes itens não forem resolvidos:

- [ ] Número de CRM (com UF) de cada autora — hoje é placeholder `CRM-XX 000000`
- [ ] Status de RQE da Marina em Medicina de Família (art. 4º, II da Res. CFM 2.336/2023)
- [ ] Revisão dos documentos legais por advogado(a)
- [ ] Link de checkout da Hotmart (preencher `HOTMART_URL` em `build/build_landing.py`)

Para tirar do noindex: `NOINDEX = False` nos dois geradores e ajustar o `robots.txt`.

## O que NUNCA entra nesta pasta

O PDF completo vendido (`dist/roteiro_completo.pdf`), o `entrega-service/`,
os fontes do miolo (`build/src/`), as fotos originais e o PDF do Carlat.
Este repositório é público.
