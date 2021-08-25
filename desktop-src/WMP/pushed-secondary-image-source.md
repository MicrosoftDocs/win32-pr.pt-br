---
title: Fonte de imagem secundária enviada por push
description: Fonte de imagem secundária enviada por push
ms.assetid: f2a2380d-c876-456b-837b-01b3997d81f2
keywords:
- Windows Media Player Aparência móvel, origem da imagem do botão
- aparência, origem da imagem do botão
- referência para capas, botões
- botões em capas, origem da imagem
- origem da imagem para capas, botões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37045da71b8417856ec72ac7e57a6a787426ba486993b9fef03910b4d32e663d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861826"
---
# <a name="pushed-secondary-image-source"></a>Fonte de imagem secundária enviada por push

Dependendo da função do botão, talvez seja necessário definir o local da imagem enviada para o estado secundário do botão. Essa será a imagem que os usuários veem quando enviam um botão de função PlayPause da segunda vez.

Para definir essa imagem, você deve inserir o tipo de imagem seguido por um espaço e o símbolo @ e outro espaço. Em seguida, você deve inserir dois inteiros positivos que definem as coordenadas superior esquerda (em pixels) da imagem que você deseja usar dentro do tipo de imagem do qual você está desenhando.

Por exemplo, para definir a imagem enviada por push para uma origem de imagem secundária, se a imagem estiver dentro do bitmap enviado por push, digite:


```C++
Pushed @ 248,0

```



Os Estados secundários não podem ter uma imagem desabilitada. As imagens secundárias devem ter a mesma largura e altura que a imagem primária.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Botões**](buttons.md)
</dt> </dl>

 

 




