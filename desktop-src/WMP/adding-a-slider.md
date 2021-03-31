---
title: Adicionando um controle deslizante
description: Adicionando um controle deslizante
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- Criando capas, controles deslizantes
- Capas, controles deslizantes do Windows Media Player
- capas, controles deslizantes
- controles deslizantes em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3efcae55b3826b69a7c88fed5a23a262526c9dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005772"
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

 

 




