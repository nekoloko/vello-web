# Vello Web para iPhone

Protótipo PWA independente, responsivo para Safari. Não precisa de Xcode para ser servido como site.

## Publicação e instalação

Sirva os arquivos desta pasta em um domínio HTTPS. No iPhone, abra a página no Safari, toque em **Compartilhar** e depois em **Adicionar à Tela de Início**. O GPS só funciona em contexto seguro (HTTPS) depois que a pessoa autoriza a localização.

## Mapas e rotas de teste

- O mapa de ruas e o cálculo de rotas de carro usam Mapbox GL JS, Geocoding API e Directions API.
- Para disponibilizar o mapa automaticamente a todos, o protótipo usa `SHARED_MAPBOX_TOKEN` no `index.html` com o token **público padrão** do Mapbox (`pk...`). Ele é visível no código público, não tem restrição de domínio e está sujeito ao limite de uso da conta; serve apenas para este teste. Não use token secreto (`sk...`).
- Sem token compartilhado no código, a engrenagem permite configurar um token local no navegador. Nunca use um token secreto (`sk...`).
- Ao tocar em **Calcular rota e solicitar**, o navegador envia ao Mapbox as coordenadas GPS e o endereço digitado para buscar o destino e montar o trajeto.
- A origem é atualizada pelo GPS do aparelho. O endereço digitado é geocodificado para uma coordenada.
- No perfil Passageiro, o mapa claro ocupa o fundo da tela e aceita arrastar com um dedo. Após autorizar a localização, um ponto azul discreto indica a posição; o trajeto usa uma linha roxa e um marcador Vello para o destino.
- Ao abrir o perfil Passageiro, o Safari solicita a localização para posicionar o ponto azul. Também é possível centralizar novamente pelo botão de localização.
- A estimativa de preço, corrida, motorista e pagamento continuam simulados; esta demo não tem navegação por voz, trânsito em tempo real nem backend.

## O que demonstra

- Perfil Passageiro e Motorista de demonstração.
- Solicitação, motorista, corrida, pagamento e ganhos simulados.
- GPS do Safari acionado pelo botão de localização.
- Preferências simples guardadas no próprio iPhone.

Não há backend, comunicação entre celulares, login ou cobrança de pagamento. Não é possível instalar esta pasta diretamente: ela precisa primeiro estar publicada em HTTPS.
