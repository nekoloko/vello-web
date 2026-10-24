# Vello Web para iPhone

Protótipo PWA independente, responsivo para Safari. Não precisa de Xcode para ser servido como site.

## Publicação e instalação

Sirva os arquivos desta pasta em um domínio HTTPS. No iPhone, abra a página no Safari, toque em **Compartilhar** e depois em **Adicionar à Tela de Início**. O GPS só funciona em contexto seguro (HTTPS) depois que a pessoa autoriza a localização.

## Mapas e rotas de teste

- O mapa de ruas e o cálculo de rotas de carro usam Mapbox GL JS, Geocoding API e Directions API.
- Na primeira abertura, toque na engrenagem do mapa e informe um token **público** do Mapbox (`pk...`). O token é guardado no `localStorage` daquele navegador; não é incluído nos arquivos do repositório.
- Restrinja o token ao domínio publicado do Vello e não use token secreto (`sk...`).
- Ao tocar em **Calcular rota e solicitar**, o navegador envia ao Mapbox as coordenadas GPS e o endereço digitado para buscar o destino e montar o trajeto.
- A origem é atualizada pelo GPS do aparelho. O endereço digitado é geocodificado para uma coordenada.
- A estimativa de preço, corrida, motorista e pagamento continuam simulados; esta demo não tem navegação por voz, trânsito em tempo real nem backend.

## O que demonstra

- Perfil Passageiro e Motorista de demonstração.
- Solicitação, motorista, corrida, pagamento e ganhos simulados.
- GPS do Safari acionado pelo botão de localização.
- Preferências simples guardadas no próprio iPhone.

Não há backend, comunicação entre celulares, login ou cobrança de pagamento. Não é possível instalar esta pasta diretamente: ela precisa primeiro estar publicada em HTTPS.
