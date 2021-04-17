---
title: Origem da imagem para TrackBar desabilitada
description: Origem da imagem para TrackBar desabilitada
ms.assetid: ecbe1670-2914-4b66-92bd-d854e6c1e897
keywords:
- Capas móveis do Windows Media Player, trackbars
- capas, trackbars
- referência para capas, trackbars
- trackbars em capas, origem da imagem
- origem da imagem para capas, trackbars
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbae540f97c7d1f7241035b074f45e6267e51615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105780223"
---
# <a name="image-source-for-disabled-trackbar"></a>Origem da imagem para TrackBar desabilitada

Você deve definir a origem da imagem que deseja exibir quando um TrackBar é desabilitado, usando o tipo de bitmap do qual você deseja desenhar a imagem. A imagem exibida geralmente estará dentro do super arquivo ou se você estiver criando uma capa para o Windows Media Player 10 Mobile, a imagem estaria dentro do arquivo SeekThumb. Você deve inserir o tipo de imagem seguido por um espaço e o símbolo @ e outro espaço. Em seguida, você deve inserir dois inteiros positivos que definem as coordenadas superior esquerda (em pixels) da imagem que você deseja usar dentro do tipo de bitmap do qual está desenhando.

Por exemplo, para usar uma imagem do bitmap SeekThumb que tem uma posição superior e esquerda de 50, 60 pixels, digite:


```C++
Disabled @ 50,60

```



Você deve definir um local de imagem para uma imagem TrackBar desabilitada. Se você não quiser exibir uma nova imagem, poderá definir a imagem de plano de fundo como sua imagem desabilitada com um deslocamento de 0, 0:


```C++
Disabled @ 50,60

```



No exemplo anterior, 50, 60 representa o local do botão com o qual você está trabalhando no arquivo SeekThumb (nesse caso, o mesmo local que o botão no bitmap em segundo plano). No entanto, é altamente recomendável que você exiba uma imagem desabilitada para todos os trackbars para dar ao usuário uma indicação visual, pois o trackbars não será utilizável em determinadas condições. Por exemplo, Seek trackbars pode ser desabilitado quando a playlist atual estiver vazia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trackbars**](trackbars.md)
</dt> </dl>

 

 




