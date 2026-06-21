# 🗳️ Urna de Votação Estudantil

PWA de urna eletrônica para eleições estudantis, inspirada na urna eletrônica brasileira.

## Estrutura

```
urna-app/
├── index.html          ← App principal (single-file)
├── manifest.json       ← PWA manifest
├── sw.js               ← Service Worker (offline)
├── favicon.ico
├── firebase.json       ← Configuração do Firebase Hosting
├── .firebaserc         ← ID do projeto Firebase
├── icons/
│   ├── icon-48.png
│   ├── icon-72.png
│   ├── icon-96.png
│   ├── icon-144.png
│   ├── icon-180.png
│   ├── icon-192.png
│   └── icon-512.png
└── .github/
    └── workflows/
        └── deploy.yml  ← Deploy automático via GitHub Actions
```

## Deploy manual

```bash
firebase login
firebase use SEU-PROJETO-FIREBASE
firebase deploy
```

## Deploy automático (GitHub Actions)

1. Vá em **Firebase Console → Project Settings → Service Accounts**
2. Gere uma nova chave privada (JSON)
3. No GitHub: **Settings → Secrets → Actions → New secret**
   - Nome: `FIREBASE_SERVICE_ACCOUNT`
   - Valor: cole o conteúdo do JSON
4. Edite `deploy.yml` e `.firebaserc` com o ID do seu projeto Firebase
5. Faça push para a branch `main` — o deploy acontece automaticamente

## PWABuilder

Após o deploy no Firebase:
1. Acesse [pwabuilder.com](https://pwabuilder.com)
2. Cole a URL do seu app Firebase
3. Gere o pacote para Android (APK/AAB), iOS ou Windows
