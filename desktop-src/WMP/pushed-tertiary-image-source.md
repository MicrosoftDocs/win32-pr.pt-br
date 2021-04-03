---
title: Fonte de imagem terciário enviada por push
description: Fonte de imagem terciário enviada por push
ms.assetid: e2d41729-87c5-4cec-931c-8702585930f2
keywords:
- Aparências móveis do Windows Media Player, origem da imagem do botão
- aparência, origem da imagem do botão
- referência para capas, botões
- botões em capas, origem da imagem
- origem da imagem para capas, botões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a37f79ab3c5fbf02eed1f0a02219a517b12ce1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916297"
---
# <a name="pushed-tertiary-image-source"></a>Fonte de imagem terciário enviada por push

A função de botão PlayPauseStop requer que você defina o local da imagem enviada para o estado terciário do botão. Essa será a imagem que os usuários veem quando enviam o botão PlayPauseStop durante o streaming de uma transmissão ao vivo.

Para definir essa imagem, você deve inserir o tipo de imagem seguido por um espaço e o símbolo @ e outro espaço. Em seguida, você deve inserir dois inteiros positivos que definem as coordenadas superior esquerda (em pixels) da imagem que você deseja usar dentro do tipo de bitmap do qual está desenhando.

Por exemplo, para definir a imagem enviada por push para uma fonte de imagem terciário, se a imagem estiver dentro do bitmap enviado por push, digite:


```C++
Pushed @ 324,0

```



Os Estados terciários não podem ter uma imagem desabilitada. São consideradas imagens terciários com a mesma largura e altura das imagens primária e secundária.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Botões**](buttons.md)
</dt> </dl>

 

 




