---
description: Retângulos de origem e de destino em renderizadores de vídeo
ms.assetid: fdddbffb-c44f-4364-9e2e-b721ba39c74f
title: Retângulos de origem e de destino em renderizadores de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556aea6aad22e5ea6df61c74ed0a46d2e3984d67
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500505"
---
# <a name="source-and-target-rectangles-in-video-renderers"></a>Retângulos de origem e de destino em renderizadores de vídeo

Há três tamanhos encontrados nas estruturas de formato [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)e [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) dos tipos de mídia de vídeo. Este artigo explica o que eles são e como eles funcionam.

Primeiro, há um tamanho no membro **bmiHeader** dessas estruturas. O membro **bmiHeader** é uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) com seus próprios membros de largura e altura, **BmiHeader. biWidth** e **bmiHeader. biHeight**.

Em segundo lugar, há um retângulo no membro **rcSource** dessas estruturas; e, por fim, há um retângulo no membro **rcTarget** dessas estruturas.

Suponha que você tenha dois filtros, A e B, e que esses filtros estejam conectados entre si (um à esquerda, ou upstream, e B à direita ou downstream) com um determinado tipo de mídia de vídeo.

Os buffers que passam entre os filtros A e B têm o tamanho (**bmiHeader. bilargura**, **BmiHeader. biHeight**). Filtrar um deve usar uma parte de seu vídeo de entrada determinado por **rcSource** e alongar esse vídeo para preencher a parte **rcTarget** do buffer. A parte do vídeo de entrada a ser usada baseia-se em como o **rcSource** se compara com o tamanho (**bilargura**, **bialtura**) do tipo de mídia que filtra a e B conectado originalmente com. Se **rcSource** estiver vazio, o filtro A usará todo o vídeo de entrada. Se **rcTarget** estiver vazio, filtrar um preencherá todo o buffer de saída.

Por exemplo, suponha que o filtro A esteja recebendo dados de vídeo com 160 x 120 pixels. Suponha também que o filtro A está conectado ao filtro B com o tipo de mídia a seguir.

-   (**bilargura**, **biHeight**): 320, 240
-   **rcSource**: (0, 0, 0, 0)
-   **rcTarget**: (0, 0, 0, 0)

Isso significa que o filtro a vai alongar o vídeo recebido por 2 nas direções x e y e preencher um buffer de saída 320 x 240.

Como outro exemplo, suponha que o filtro A esteja recebendo dados de vídeo 160 x 120 e que esteja conectado ao filtro B com o seguinte tipo de mídia.

-   (**bilargura**, **biHeight**): 320, 240
-   **rcSource**: (0, 0, 160, 240)
-   **rcTarget**: (0, 0, 0, 0)

O membro **rcSource** é relativo ao tamanho do buffer conectado de 320, 240. Porque o **rcSource** especificado (0, 0, 160, 240) é a metade esquerda do buffer, o filtro a terá a metade esquerda de seu vídeo de entrada ou a parte (0, 0, 80, 120) e alongará o vídeo para um tamanho de (320, 240) (por 4 na direção x e por 2 na direção y) e preenchendo o buffer de saída 320 x 240.

Agora suponha que o filtro A chama [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md)e o exemplo de mídia retornado tenha um tipo de mídia anexado a ele, o que significa que o filtro B deseja filtrar um para fornecer um tamanho ou tipo de vídeo diferente do que o fornecido anteriormente. Suponha que o novo tipo de mídia seja:

-   (**bilargura**, **biHeight**): 640, 480
-   **rcSource**: (0, 0, 160, 120)
-   **rcTarget**: (0, 0, 80, 60)

Isso significa que o exemplo de mídia tem um buffer que tem 640 x 480 de tamanho. O membro **rcSource** é relativo ao tipo de mídia original conectada (320, 240) para o novo tipo de mídia de (640, 480); portanto, **rcSource** especifica que o canto superior esquerdo (25%) do vídeo de entrada deve ser usado. Essa parte do vídeo de entrada é colocada nos pixels superior esquerdo (80, 60) do buffer de saída 640 x 480, conforme especificado por **rcTarget** de (0, 0, 80, 60). Como o filtro A está recebendo 160 x 120 vídeo, o canto superior esquerdo do vídeo de entrada é uma parte (80, 60), o mesmo tamanho do bitmap de saída e nenhum alargamento é necessário.

Filtrar um não colocará nenhum dado nos outros pixels do buffer de saída e deixará esses bits inalterados. O membro **rcSource** é limitado pela **bilargura** e pela **altura** do tipo de mídia original conectada entre os filtros A e B, e **rcTarget** é limitado pela nova **bilargura** e pela mesma **altura** do exemplo de mídia. No exemplo anterior, **rcSource** não pôde ficar fora dos limites de (0, 0, 320, 240) e **rcTarget** não pôde ficar fora dos limites de (0, 0, 640, 480).

 

 



