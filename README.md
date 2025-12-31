# First Frame Studio

Interface React/Vite + Tailwind para gerar prompts cinematográficos (frame e vídeo), com tradução automática, refinamento criativo e análise de imagem (Gemini).

## Requisitos
- Node.js 18+ (recomendado 20+)

## Instalação
```bash
npm install
```

## Variáveis de ambiente
Crie um `.env.local` na raiz (já listado no `.gitignore`) copiando de `.env.example`:
```
VITE_GEMINI_API_KEY=YOUR_GEMINI_API_KEY
```

## Desenvolvimento
```bash
npm run dev
```
Abra a URL exibida pelo Vite (tipicamente `http://localhost:5173`).

## Build
```bash
npm run build
```
Saída em `dist/`.

## Preparar push para GitHub
1. Garanta que o `.env.local` **não** seja commitado (já está no `.gitignore`).
2. Confira o status: `git status`.
3. Faça o commit inicial:
   ```bash
   git add .
   git commit -m "feat: first-frame-studio app"
   ```
4. Crie o repositório remoto no GitHub e conecte:
   ```bash
   git branch -M main
   git remote add origin git@github.com:<user>/<repo>.git
   git push -u origin main
   ```

## Deploy (opcional)
- Qualquer host estático que sirva `dist` funciona (Vercel, Netlify, GitHub Pages). Em Vercel:
  - Build Command: `npm run build`
  - Output: `dist`
  - Env: `VITE_GEMINI_API_KEY`
