---
title: Fonte de imagem secundária normal
description: Fonte de imagem secundária normal
ms.assetid: fe5c0da2-0c40-456f-ab56-ac61ed69ff2d
keywords:
- Aparências móveis do Windows Media Player, origem da imagem do botão
- aparência, origem da imagem do botão
- referência para capas, botões
- botões em capas, origem da imagem
- origem da imagem para capas, botões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ff828f6d0f0c8348453cb00fef04ab31718693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781359"
---
# <a name="normal-secondary-image-source"></a>Fonte de imagem secundária normal

Dependendo da função do botão, talvez seja necessário definir o local da imagem normal para o estado secundário do botão. Essa será a imagem que os usuários veem quando enviam por push um botão de função PlayPause na primeira vez.

Para definir essa imagem, você deve inserir o tipo de imagem seguido por um espaço e o símbolo @ e outro espaço. Em seguida, você deve inserir dois inteiros positivos que definem as coordenadas superior esquerda (em pixels) da imagem que você deseja usar dentro do tipo de bitmap do qual está desenhando.

Por exemplo, para definir a imagem normal para uma origem de imagem secundária, se a imagem estiver dentro do bitmap enviado por push, digite:


```C++
Pushed @ 210,0

```



Os Estados secundários não podem ter uma imagem desabilitada. As imagens secundárias devem ter a mesma largura e altura que a imagem primária.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Botões**](buttons.md)
</dt> </dl>

 

 




