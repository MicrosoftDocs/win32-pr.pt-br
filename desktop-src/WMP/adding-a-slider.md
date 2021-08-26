---
title: Adicionando um controle deslizante
description: Adicionando um controle deslizante
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- Criando capas, controles deslizantes
- Windows Media Player capas, controles deslizantes
- capas, controles deslizantes
- controles deslizantes em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c3644e1b243188664295bbc00101a74377cbef17632217ff0a81dac0d377a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004375"
---
# <a name="adding-a-slider"></a>Adicionando um controle deslizante

Você pode adicionar um controle deslizante para mostrar a posição atual da mídia e também permitir que o usuário altere a posição no arquivo de mídia atual.

Primeiro, você deve adicionar o elemento **Slider** :


```C++
<SLIDER
  id = "myslider"
  min = "0"
  max = "wmpprop:player.currentMedia.duration"
  onmouseup = "player.controls.currentPosition = myslider.value; "
  tooltip = "current position"
  height = "10"
  width = "180"
  top = "150"
  left = "88"
  backgroundColor = "red"
  foregroundColor = "blue"
  thumbImage = "thumb.bmp"/>

```



Isso define um valor máximo com base na duração do arquivo de mídia atual. Isso usa um pequeno bitmap de imagem Thumb que é apenas 10 pixels por um quadrado verde de 10 pixels. O plano de fundo do controle deslizante será vermelho e o primeiro plano será azul. Quando o usuário arrasta a imagem em miniatura para uma nova posição e deixa o botão do mouse, a mídia muda para essa posição.

Mas o controle deslizante não se moverá por si só, a menos que você meça a posição atual com o atributo **\_ onChange CurrentPosition** do elemento **Controls** , que é inserido no elemento **Player** .


```C++
<PLAYER
    URL = "https://proseware.com/laure.wma">

    <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition; "/>

</PLAYER>

```



Quando a posição da mídia é alterada, isso dispara um evento que executa a linha de código que altera o valor do controle deslizante para a posição atual da mídia.

Você pode ver uma aparência de controle deslizante de trabalho semelhante na seção de exemplo do SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de criação de capa**](skin-creation-guide.md)
</dt> </dl>

 

 




