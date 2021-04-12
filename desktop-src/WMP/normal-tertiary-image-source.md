---
title: Fonte de imagem terciário normal
description: Fonte de imagem terciário normal
ms.assetid: ce0b009a-b008-4e8b-875b-b2ff3c1c0b81
keywords:
- Aparências móveis do Windows Media Player, origem da imagem do botão
- aparência, origem da imagem do botão
- referência para capas, botões
- botões em capas, origem da imagem
- origem da imagem para capas, botões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109509914c498e950f148caf7c260ef814c1074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364293"
---
# <a name="normal-tertiary-image-source"></a>Fonte de imagem terciário normal

A função de botão PlayPauseStop requer que você defina o local da imagem normal para o estado terciário do botão. Essa será a imagem que os usuários veem depois de enviarem por push o botão PlayPauseStop para começar a transmitir uma transmissão ao vivo.

Para definir essa imagem, você deve inserir o tipo de imagem seguido por um espaço e o símbolo @ e outro espaço. Em seguida, você deve inserir dois inteiros positivos que definem as coordenadas superior esquerda (em pixels) da imagem que você deseja usar dentro do tipo de bitmap do qual está desenhando.

Por exemplo, para definir a imagem normal para uma fonte de imagem terciário, se a imagem estiver dentro do bitmap enviado por push, digite:


```C++
Pushed @ 286,0

```



Os Estados terciários não podem ter uma imagem desabilitada. São consideradas imagens terciários com a mesma largura e altura das imagens primária e secundária.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Botões**](buttons.md)
</dt> </dl>

 

 




