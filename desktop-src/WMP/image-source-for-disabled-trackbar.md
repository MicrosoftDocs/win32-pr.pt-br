---
title: Origem da imagem para a barra de faixa desabilitada
description: Origem da imagem para a barra de faixa desabilitada
ms.assetid: ecbe1670-2914-4b66-92bd-d854e6c1e897
keywords:
- Windows Media Player Capas móveis, barras de faixa
- skins,trackbars
- referência para capas, barras de faixa
- trackbars in skins,image source
- fonte de imagem para capas, barras de faixa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b3f5f58198d55f2dcd17b23b102c91eb4dff4787489e13775c6be71faa3223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338941"
---
# <a name="image-source-for-disabled-trackbar"></a>Origem da imagem para a barra de faixa desabilitada

Você deve definir a origem da imagem que deseja exibir quando uma barra de faixa estiver desabilitada, usando o tipo de bitmap do qual você deseja desenhar a imagem. A imagem exibida geralmente estará dentro do arquivo Super ou, se você estiver criando uma capa para o Windows Media Player 10 Mobile, a imagem estará dentro do arquivo SeekThumb. Você deve inserir o tipo de imagem seguido por um espaço e o símbolo @ e outro espaço. Em seguida, você deve inserir dois inteiros positivos que definem as coordenadas superior esquerda (em pixels) da imagem que você deseja usar dentro do tipo de bitmap do qual você está desenhando.

Por exemplo, para usar uma imagem do bitmap SeekThumb que tem uma posição superior e esquerda de 50,60 pixels, digite:


```C++
Disabled @ 50,60

```



Você deve definir um local de imagem para uma imagem de barra de faixa desabilitada. Se você não quiser exibir uma nova imagem, poderá definir a imagem tela de fundo como sua imagem Desabilitada com um deslocamento de 0,0:


```C++
Disabled @ 50,60

```



No exemplo anterior, 50,60 representa o local do botão com o que você está trabalhando no arquivo SeekThumb (nesse caso, o mesmo local que o botão no bitmap de plano de fundo). No entanto, é altamente recomendável exibir uma imagem Desabilitada para todas as barras de faixa para dar ao usuário uma indicação visual, pois as barras de faixa não serão usadas em determinadas condições. Por exemplo, as barras de faixa seek podem ser desabilitadas quando a playlist atual está vazia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trackbars**](trackbars.md)
</dt> </dl>

 

 




