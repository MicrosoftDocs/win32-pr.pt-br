---
title: Origem da imagem enviada por push
description: Origem da imagem enviada por push
ms.assetid: 6cc290d8-2c15-4789-970d-9a3663a64d08
keywords:
- Aparências móveis do Windows Media Player, origem da imagem do botão
- aparência, origem da imagem do botão
- referência para capas, botões
- botões em capas, origem da imagem
- origem da imagem para capas, botões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021c77a305e0f6981823c8a1e471862554c32e08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636253"
---
# <a name="pushed-image-source"></a>Origem da imagem enviada por push

Você deve definir a origem da imagem que deseja exibir quando o usuário envia um botão. A imagem é proveniente do arquivo definido como enviado por push na seção bitmaps. Você deve inserir o tipo de imagem seguido por um espaço e o símbolo @ e outro espaço. Em seguida, você deve inserir dois inteiros positivos que definem as coordenadas superior e esquerda (em pixels) da imagem que você deseja usar dentro do arquivo de imagem enviado por push. O local no qual a imagem será exibida vem das coordenadas definidas para o botão em relação à imagem de plano de fundo; Mas o local de origem é definido pelos dois números após "Push @" e é relativo à imagem enviada por push da qual você está lendo a imagem.

Por exemplo, para usar uma imagem da imagem enviada por push que está no arquivo enviado cujo local superior esquerdo é 50, 60, você usaria o seguinte código:


```C++
Pushed @ 50,60

```



Se você não quiser exibir uma imagem diferente, poderá definir o bitmap de plano de fundo como seu bitmap enviado por push. Para fazer isso, especifique o arquivo de plano de fundo como o arquivo enviado por push e especifique o deslocamento no canto superior esquerdo do botão:


```C++
Pushed @ 50,60

```



Se você fizer isso, nenhum dos botões poderá exibir uma imagem enviada por push. É recomendável exibir uma imagem enviada por push para todos os botões para dar ao usuário uma indicação visual, pois nem sempre fica claro se um toque produz um resultado, especialmente quando a música está sendo reproduzida ou quando o som de toque está desativado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Botões**](buttons.md)
</dt> </dl>

 

 




