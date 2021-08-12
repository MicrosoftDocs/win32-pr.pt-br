---
title: Origem de imagem secundária normal
description: Origem de imagem secundária normal
ms.assetid: fe5c0da2-0c40-456f-ab56-ac61ed69ff2d
keywords:
- Windows Media Player Capas móveis, origem da imagem do botão
- capas, origem da imagem do botão
- referência para capas, botões
- botões em capas, origem da imagem
- fonte da imagem para capas, botões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f6aeb48ceabc873d4aeb0db910db896712fe16377aa0f67b76205ad8a39c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573726"
---
# <a name="normal-secondary-image-source"></a>Origem de imagem secundária normal

Dependendo da função de botão, talvez seja necessário definir o local da imagem normal para o estado secundário do botão. Essa será a imagem que os usuários veem ao efetuar push de um botão de função PlayPause pela primeira vez.

Para definir essa imagem, você deve inserir o tipo de imagem seguido por um espaço, o símbolo @ e outro espaço. Em seguida, você deve inserir dois inteiros positivos que definem as coordenadas superior esquerda (em pixels) da imagem que você deseja usar dentro do tipo de bitmap do qual você está desenhando.

Por exemplo, para definir a imagem normal para uma origem de imagem secundária, se a imagem estiver dentro do bitmap por pushed, digite:


```C++
Pushed @ 210,0

```



Estados secundários não podem ter uma imagem Desabilitada. Supõe-se que as imagens secundárias sejam da mesma largura e altura que a imagem primária.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Botões**](buttons.md)
</dt> </dl>

 

 




