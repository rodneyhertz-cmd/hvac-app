# Ferramentas HVAC-R – app Android

Mesmo app da página web, com leitura **nativa** do magnetômetro (não depende do flag do Chrome).

## Gerar o APK (sem instalar nada no PC)
1. Crie um repositório vazio no GitHub (github.com > New repository).
2. Envie todo o conteúdo desta pasta para ele (botão "Add file > Upload files", arrastando as pastas
   `www`, `android`, `.github` e os arquivos soltos). Se a pasta `.github` não subir pelo navegador,
   use o GitHub Desktop ou `git push`.
3. Abra a aba **Actions**, escolha **Gerar APK** e clique em **Run workflow**.
4. Em ~5 minutos, abra a execução concluída e baixe **hvac-tools-apk** (Artifacts). Descompacte: dentro está o `app-debug.apk`.
5. Passe o APK para o celular e instale (permita "instalar apps desconhecidos" quando o Android pedir).

## Gerar localmente (opcional)
Requer Node 22, JDK 21 e Android SDK: `npm install && npx cap sync android && cd android && ./gradlew assembleDebug`.

## Atualizar a página do app
Edite `www/index.html`, envie ao GitHub e rode o workflow de novo.

Código do sensor nativo: `android/app/src/main/java/com/rodneyhertz/hvactools/MagnetPlugin.java`.
