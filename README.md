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

O site está com `<meta name="robots" content="noindex,nofollow">`. **É essa meta tag que
segura o site fora do Google** — o `robots.txt` daqui é inerte em Pages de projeto
(crawlers só leem o robots.txt da raiz do domínio); ver os comentários no próprio arquivo.

Ele **não deve sair do noindex** enquanto estes itens não forem resolvidos:

- [x] CRM da **Julia** — `CRM-SP 285002` (08/08/2026)
- [x] CRM da Marina — `CRM-BA 41016 · CRM-SP 285066` (07/08/2026)
- [x] RQE da Marina em Medicina de Família — `RQE 27384` no CREMEB (07/08/2026).
      O RQE **não migra** para a inscrição de SP; se for registrado lá também,
      atualizar `RQE_MARINA` em `build/build_landing.py`.
- [ ] Revisão dos documentos legais por advogado(a)
- [ ] Link de checkout da Hotmart (preencher `HOTMART_URL` em `build/build_landing.py`)

Para tirar do noindex: `NOINDEX = False` nos dois geradores. O `robots.txt` já está
em modo de lançamento (rastreio liberado) — não precisa mexer.

## O que NUNCA entra nesta pasta

O PDF completo vendido (`dist/roteiro_completo.pdf`), o `entrega-service/`,
os fontes do miolo (`build/src/`), as fotos originais e o PDF do Carlat.
Este repositório é público.
