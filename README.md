# Publicar no GitHub Pages

1. Envie o repositório para o GitHub.
2. No repositório, abra **Settings → Pages**.
3. Em **Build and deployment**, selecione **Deploy from a branch**, escolha a branch principal e a pasta **/(root)**, então salve.
4. Aguarde a publicação e abra a URL indicada nessa tela. Para um repositório de projeto, ela terá o formato `https://<usuario>.github.io/<repositorio>/`.
5. Teste o slider e confirme que a foto carrega. O caminho `./assets/tiffany.webp` é relativo e funciona tanto na raiz quanto sob o caminho do repositório.

## Analytics e limitações

O Google tag do GA4 está configurado em `index.html`. Teste o evento `telegram_outbound` no GA4 DebugView após publicar e marque-o como evento principal no GA4 se ele for a conversão usada nas campanhas; atualize também a importação/conversão no Google Ads, se aplicável. Ele mede uma tentativa de encaminhamento ao Telegram, não confirma que a pessoa entrou no canal. Como o redirecionamento é imediato, teste também se o evento chega em navegadores reais.

GitHub Pages é hospedagem estática: este repositório não implementa rate limiting nem validação anti-bot no servidor. O filtro no navegador reduz apenas eventos sintéticos simples; automação de navegador e requests HTTP diretos ainda podem passar.