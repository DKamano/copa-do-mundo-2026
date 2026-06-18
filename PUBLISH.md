# Como publicar este site

Opções para publicar o `index.html` deste repositório.

## 1) Visualizar localmente

Abra um terminal e rode:

```bash
cd /workspaces/copa-do-mundo-2026
python3 -m http.server 8000
# abra http://localhost:8000 no navegador
```

## 2) Publicar usando GitHub Pages (recomendado)

- Faça commit e push do arquivo `index.html` para o repositório remoto.
- No GitHub: vá em *Settings → Pages*, selecione a branch (por exemplo `main`) e a pasta `/ (root)`, e salve.
- O site ficará disponível em `https://<usuario>.github.io/<repo>` ou no domínio customizado configurado.

Alternativa: publicar na branch `gh-pages`:

```bash
git checkout --orphan gh-pages
git rm -rf .
cp ../copa-do-mundo-2026/index.html .
git add index.html
git commit -m "Deploy GitHub Pages"
git push -u origin gh-pages
```

## 3) CI/CD (GitHub Actions)

Você também pode configurar um workflow para gerar e publicar o site automaticamente em `gh-pages`.

---

Se quiser, eu posso criar um workflow de GitHub Actions que publica automaticamente ao fazer push. Deseja que eu adicione isso?
