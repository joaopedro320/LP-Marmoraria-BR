# Marmoraria BR — LP para Vercel

## Deploy rápido

1. Suba a pasta inteira (`index.html`, `robots.txt`, `sitemap.xml`, a pasta `images/` e este README) pra Vercel.
2. **Add New → Project → Deploy** e arraste a pasta, ou rode `vercel` dentro dela pelo terminal. Não precisa de build, é HTML puro.
3. Depois do deploy, aponte o domínio `brmarmoraria.com` pro projeto na Vercel (Settings → Domains).

## O que já está resolvido nesta versão

- **Fotos reais**: as 29 fotos que você mandou (do @marmoraria_br) estão aplicadas na aba de Portfólio, com filtro por categoria (Cozinhas, Banheiros, Escadarias, Fachadas, Showroom, Ambientes) e lightbox ao clicar. Fiquei de fora só das fotos de "zezinho_moveisplanejados" e "elite_moveisplanejados" que vieram no zip, porque são de outras empresas (marcenaria), não da Marmoraria BR.
- **Logo real**: a logo redonda que você mandou está no header e no rodapé (`images/logo.png`), e gerei um favicon (`images/favicon.png`) e uma imagem de compartilhamento (`images/og-image.jpg`) a partir dela e de uma das fotos reais.
- **Headline**: "Marmoraria de Alto Padrão perto de você!"
- **Todos os botões de conversão** (WhatsApp no header, hero, oferta, CTA final e botão flutuante) usam a mensagem: *"Olá vi o site no google e gostaria de solicitar um orçamento."*
- **Responsivo**: breakpoints ajustados pra mobile, tablet (860px e 1024px) e desktop, com a galeria de portfólio em grid fluido que se adapta a qualquer largura sem quebrar.

## O que ainda falta antes de publicar de verdade

**Legendas das fotos.** Categorizei as 29 fotos por tipo de ambiente (cozinha, banheiro, escadaria, fachada, showroom) com base no que dava pra ver em cada imagem, mas eu não sei o nome exato da pedra usada em cada obra nem o nome do cliente. Se quiser legendas mais específicas (nome da pedra, cidade da obra), me passe a lista e eu atualizo.

**Endereço da loja.** O schema de SEO (`LocalBusiness`) no `<head>` está com `"PREENCHER endereço da loja/fábrica"`. Preencha com o endereço comercial real (não usei o endereço pessoal da Nara que estava no formulário de domínio, esse é dado pessoal, não da empresa).

**Depoimentos.** A seção "Depoimentos" ainda está com 3 placeholders `[INSERIR DEPOIMENTO]`. Nunca inventar depoimento: peça pra Annalice separar 3 avaliações reais (nome, ambiente executado, e se possível foto) e um print das avaliações do Google Meu Negócio antes do ar.

**Fontes da marca.** Vonique 92 e NEHAD (as fontes do brand book) são gratuitas só pra uso pessoal, cada uma tem link de licença comercial (Sharkshock e Creative Fabrica). Usei Fraunces + Manrope (Google Fonts, gratuitas e sem restrição comercial) como substitutas fiéis ao espírito da marca. Se comprar a licença comercial das fontes originais, é só trocar o `@import` do Google Fonts por `@font-face` com os arquivos `.woff2` licenciados.

**GTM.** Deixei um evento `clique_whatsapp` disparando pro `dataLayer` a cada clique nos botões, comentado no fim do arquivo. É só descomentar as 2 linhas do `dataLayer`/`gtag` no `<head>` do jeito que preferir e colocar o ID do GTM quando tiver.

## Checklist de SEO já aplicado

- Title e meta description com palavra-chave + cidade
- URL canônica e Open Graph com imagem real
- Schema.org `HomeAndConstructionBusiness` com horário de atendimento, telefone e cidades atendidas (Sidrolândia, Maracaju, Jardim, Bonito)
- Hierarquia de headings (H1 único, H2 por seção)
- `robots.txt` e `sitemap.xml` inclusos
- Todas as fotos com `alt` descritivo (nome do ambiente + "Marmoraria BR"), `loading="lazy"` e compressão JPEG otimizada (a pasta `images/` inteira ficou com ~5MB pras 29 fotos + logo, leve pro tamanho)
- Textos com os termos que o cliente levantou no briefing: pedra natural, granito, quartzito, revestimento, rebaixo italiano, compactado de quartzo

## Ângulo da copy

Foi montada com dois ângulos, principal e secundário, como você confirmou:
- **Principal:** ambientes residenciais de alto padrão com segurança e prazo garantido
- **Secundário:** revestimentos naturais decorativos (moledo, rock face, travertino), seção própria mais abaixo na página, agora também com fotos reais de fachada

Se quiser inverter a ordem ou dar mais peso a um dos dois, é só avisar.
