# Fuga da Chinelada — APK Android

Jogo 3D de fuga: Yunah ou Yota tenta sair de casa sem a mamãe ver.

## Como gerar o APK pelo GitHub (sem instalar nada no computador)

1. Crie um repositório novo no GitHub (pode ser privado).
2. Envie **todos** os arquivos desta pasta, mantendo as pastas como estão:
   - `www/index.html`
   - `package.json`
   - `capacitor.config.json`
   - `.github/workflows/build-apk.yml`
   - `README.md`

   Pelo site: **Add file → Upload files** e arraste a pasta inteira.
   Atenção: a pasta `.github` começa com ponto e às vezes fica escondida no
   computador/celular. Se ela não subir, crie o arquivo direto no GitHub em
   **Add file → Create new file** com o nome `.github/workflows/build-apk.yml`
   e cole o conteúdo.
3. Abra a aba **Actions** do repositório. O processo **Gerar APK** começa
   sozinho a cada envio (ou clique em **Run workflow**). Leva uns 5 minutos.
4. Quando ficar verde ✅, clique nele e, lá embaixo em **Artifacts**, baixe
   `fuga-da-chinelada-apk`. Vem um `.zip` com o `app-debug.apk` dentro.
5. No celular, abra o `.apk` e permita "instalar apps desconhecidos".

## Observações

- O motor 3D (three.js) é baixado automaticamente durante a compilação e vai
  dentro do app, então o jogo funciona sem internet. As fontes vêm do Google
  Fonts: sem internet o jogo usa a fonte do sistema.
- É um APK de teste (debug), ótimo para instalar no seu celular. Para publicar
  na Play Store é preciso um APK/AAB assinado.
- Para trocar o nome ou o ID do app, edite `capacitor.config.json`.
- Para atualizar o jogo, substitua `www/index.html` e envie de novo.
