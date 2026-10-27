# Milkymix — site responsivo

Site estático em um único arquivo (`index.html`), preparado para celular Android e desktop. Não precisa instalar Node.js nem configurar servidor: basta abrir o arquivo no navegador ou publicar a pasta em uma hospedagem estática.

## Recursos incluídos
- Layout responsivo com menu mobile, cards de sabores e seções promocionais.
- Carrinho funcional com quantidades, remoção, subtotal e persistência local no navegador.
- Desconto de 20% aplicado automaticamente quando o carrinho tem 2 ou mais milkshakes.
- Finalização por WhatsApp, montando a mensagem com sabores, quantidades e valores.
- Animações leves, acessibilidade básica e respeito à preferência por movimento reduzido.

## Configurar o WhatsApp da loja
Abra `index.html`, vá ao final do arquivo e procure:

```js
const WHATSAPP_NUMBER = "";
```

Coloque o número com código do país e DDD, somente números. Exemplo fictício: `5584999999999`. Antes de publicar, troque também os preços, descrições, nomes e textos de demonstração pelos dados reais da loja.

## Imagens
As fotos estão apontadas para URLs externas, então a conexão com a internet é necessária para carregá-las. Troque os links no HTML e na constante `PRODUCTS` no JavaScript pelas fotos autorizadas da própria loja para garantir consistência e direitos de uso.

## Abrir no Termux
Salve `index.html` em uma pasta e execute, de dentro dela:

```sh
python -m http.server 8080 --bind 127.0.0.1
```

Depois abra `http://127.0.0.1:8080` no navegador do Android. Para testar em outro dispositivo conectado à mesma rede, use o IP local do telefone em vez de `127.0.0.1`.
