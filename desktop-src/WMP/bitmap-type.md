---
title: Tipo de bitmap
description: Tipo de bitmap
ms.assetid: 208df4b9-d1be-49ff-bc0b-2e000608e9c7
keywords:
- Capas do Windows Media Player Mobile, bitmaps
- capas, bitmaps
- referência para capas, bitmaps
- bitmaps em capas, tipos
- bitmaps em capas, valores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 602a436b5f4428b897672607265098104a9c1b0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822615"
---
# <a name="bitmap-type"></a>Tipo de bitmap

A tabela a seguir mostra os valores válidos para o tipo de bitmap. Somente o tipo de plano de fundo é necessário; outras são opcionais e estão relacionadas a diferentes usos de imagens possíveis.



| Valor       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tela de fundo  | Obrigatórios. A imagem na qual todas as imagens de botão são sobrepostas. As dimensões da imagem de plano de fundo base incluem a largura e a altura totais da tela. Esse também é o arquivo em que as imagens para os Estados naturais dos botões e trackbars são exibidas. (Botões enviados por push e desabilitados não fazem parte desta imagem.)                                                                                                                                                                                                                                                                                           |
| Desabilitado    | Obrigatórios. Indica que o envio do botão não terá efeito. Define uma imagem que é exibida quando a funcionalidade específica do Player não está disponível para o usuário. Você deve fornecer um valor de coordenadas para indicar a posição do canto superior esquerdo dessa imagem em relação à imagem de plano de fundo.                                                                                                                                                                                                                                                                                                                |
| Colocada      | Obrigatórios. Define uma imagem que é exibida quando o usuário envia um botão. Use push para fornecer comentários visuais ao usuário quando ele toca em um botão. Você deve fornecer um valor de coordenadas para indicar a posição do canto superior esquerdo dessa imagem em relação à imagem de plano de fundo.                                                                                                                                                                                                                                                                                                                              |
| Região      | Define imagens que usam regiões coloridas para representar a área de toque-resposta para os botões de tipo de acesso: PushHit, ToggleHit, 2PushHit. Se você estiver usando os botões de tipo de acesso, deverá fornecer uma imagem de região. Esse arquivo de imagem usa cores de paleta específicas do Windows para cada controle. As cores são definidas por números que representam o valor de vermelho, verde e azul para a região. Essa imagem nunca é vista pelo usuário. Você também deve fornecer um valor de coordenadas para indicar a posição do canto superior esquerdo dessa imagem em relação à imagem de plano de fundo.                                                      |
| SeekThumb   | Define uma imagem que será usada em conjunto com um TrackBar para indicar a posição atual no item de mídia. Por exemplo, se uma música for concluída por meia execução, a imagem SeekThumb será exibida no meio do TrackBar. Ao tocar e arrastar a imagem SeekThumb, o usuário pode reiniciar o item de mídia em qualquer posição, que é chamada de *busca*. A imagem do TrackBar em si é definida na imagem de plano de fundo. A imagem SeekThumb não está incluída na seção bitmaps do arquivo de definição de capa, mas é especificada como parte da definição de TrackBar na seção TrackBars. |
| Super       | Define a imagem desabilitada para um TrackBar. Ele também pode conter imagens alternativas para o botão mudo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| VolumeThumb | Define uma imagem a ser usada em conjunto com um TrackBar para indicar a posição do volume. Ao tocar e arrastar a imagem VolumeThumb, o usuário pode alterar o nível de volume. A imagem do TrackBar em si é definida na imagem de plano de fundo. A imagem VolumeThumb não está incluída na seção bitmaps do arquivo de definição de capa, mas é especificada como parte da definição de TrackBar na seção TrackBars.                                                                                                                                                                                      |



 

> [!Note]  
> Os tipos de região e superbitmap são preteridos em capas para Windows Media Player 10 Mobile ou posterior.

 

Observe que o nome do arquivo e o tipo de arquivo não são necessariamente os mesmos. Você pode chamar o arquivo enviado por push, mas ele ainda é referenciado em outros lugares como enviado por push. Por exemplo, na seção botões, você terá um item como:


```C++
Pushed @ 50,60

```



Isso se refere ao tipo do arquivo, não ao nome do arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Bitmaps**](bitmaps.md)
</dt> </dl>

 

 




