# Upload Widget Server — FTR (Rocketseat)

Projeto da **Faculdade de Tecnologia Rocketseat (FTR)** para praticar construção de uma API simples de upload de imagens. A ideia é enviar um arquivo via `multipart/form-data`, armazenar no Cloudflare R2 e receber de volta a URL pública.

## Tecnologias
- Node.js + TypeScript
- Fastify (HTTP, CORS, multipart)
- AWS SDK v3 (compatível com R2)
- Zod (validação de ambiente e payload)

## Como rodar
1. Duplique o `.env.example` para `.env` e preencha credenciais do R2:
   - `CLOUDFLARE_ACCESS_KEY_ID`
   - `CLOUDFLARE_SECRET_ACCESS_KEY`
   - `CLOUDFLARE_BUCKET`
   - `CLOUDFLARE_ACCOUNT_ID`
   - `CLOUDFLARE_PUBLIC_URL` (base pública do bucket)
2. Instale deps: `npm install`
3. Inicie: `npm run dev`

### Teste rápido
Use `curl` enviando um arquivo qualquer:
```bash
curl -F "file=@/caminho/para/arquivo.png" http://localhost:3333/uploads
```
Resposta esperada: `{"url":"<url-publica>"}`.

## Quer praticar recriando manualmente?
Criei um prompt em `prompt/manual-recreation.md` para usar no Codex/Cursor. Ele guia, passo a passo, como reconstruir o commit manualmente (criando pastas, arquivos e entendendo os conceitos). Útil para estudar o fluxo com apoio da IA sem precisar clonar.

---
Sinta-se à vontade para clonar, modificar e usar como base de estudos. Bons uploads!
