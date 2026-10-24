# Vello Web para iPhone

Protótipo PWA independente, responsivo para Safari. Não precisa de Xcode para ser servido como site.

## Publicação e instalação

Sirva os arquivos desta pasta em um domínio HTTPS. No iPhone, abra a página no Safari, toque em **Compartilhar** e depois em **Adicionar à Tela de Início**. O GPS só funciona em contexto seguro (HTTPS) depois que a pessoa autoriza a localização.

## Mapas e rotas de teste

- O mapa de ruas e o cálculo de rotas de carro usam Mapbox GL JS, Geocoding API e Directions API.
- Para disponibilizar o mapa automaticamente a todos, o protótipo usa `SHARED_MAPBOX_TOKEN` no `index.html` com o token **público padrão** do Mapbox (`pk...`). Ele é visível no código público, não tem restrição de domínio e está sujeito ao limite de uso da conta; serve apenas para este teste. Não use token secreto (`sk...`).
- Sem token compartilhado no código, a engrenagem permite configurar um token local no navegador. Nunca use um token secreto (`sk...`).
- No perfil Passageiro, a tela inicial deixa o mapa em destaque e mostra o botão **Pedir corrida**. O mapa aceita arrastar com um dedo e mostra a localização atual como um ponto roxo animado.
- Ao abrir o pedido, a origem usa a localização do GPS e pode ser editada. O campo de destino aceita um endereço ou abre o seletor do mapa: arraste até o ponto desejado e toque em **Concluir local**. O app mostra o endereço encontrado e usa as coordenadas exatas do ponto escolhido na rota.
- O navegador envia ao Mapbox a localização/destino necessários quando a pessoa pede a rota; a coordenada do mapa é consultada para obter o endereço depois de tocar em **Concluir local**. A rota aparece em roxo com marcadores próprios do Vello.
- O iPhone pede permissão de localização ao abrir o perfil Passageiro; o botão de localização também pode reposicionar o mapa.
- A estimativa de preço, corrida, motorista e pagamento continuam simulados; esta demo não tem navegação por voz, trânsito em tempo real nem backend.

## O que demonstra

- Perfil Passageiro e Motorista de demonstração.
- Solicitação, motorista, corrida, pagamento e ganhos simulados.
- GPS do Safari, origem editável e destino selecionável no mapa.
- Preferências simples guardadas no próprio iPhone.

Não há backend, comunicação entre celulares, login ou cobrança de pagamento. Não é possível instalar esta pasta diretamente: ela precisa primeiro estar publicada em HTTPS.
