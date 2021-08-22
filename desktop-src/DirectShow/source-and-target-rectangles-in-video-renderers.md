---
description: Retângulos de origem e destino em renderadores de vídeo
ms.assetid: fdddbffb-c44f-4364-9e2e-b721ba39c74f
title: Retângulos de origem e destino em renderadores de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020be0786a071c6bbdf33649405517ed3788789268052b61ee89d97a23f357f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072540"
---
# <a name="source-and-target-rectangles-in-video-renderers"></a>Retângulos de origem e destino em renderadores de vídeo

Há três tamanhos encontrados nas estruturas de formato [**VIDEOINFO,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)e [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) de tipos de mídia de vídeo. Este artigo explica o que são e como funcionam.

Primeiro, há um tamanho no membro **bmiHeader** dessas estruturas. O **membro bmiHeader** é uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) com seus próprios membros de largura e altura, **bmiHeader.biWidth** e **bmiHeader.biHeight**.

Em segundo lugar, há um retângulo no **membro rcSource** dessas estruturas; e, por fim, há um retângulo no **membro rcTarget** dessas estruturas.

Suponha que você tenha dois filtros, A e B, e que esses filtros estão conectados uns aos outros (A à esquerda, upstream e B à direita ou downstream) com um determinado tipo de mídia de vídeo.

Os buffers que passam entre os filtros A e B têm o tamanho (**bmiHeader.biWidth**, **bmiHeader.biHeight**). O filtro A deve pegar uma parte de seu vídeo de entrada determinado por **rcSource** e alongar esse vídeo para preencher a parte **rcTarget** do buffer. A parte do vídeo de entrada a ser usada baseia-se em como **rcSource** se compara ao tamanho (**biWidth**, **biHeight**) do tipo de mídia que filtra A e B originalmente conectados. Se **rcSource estiver** vazio, o filtro A usará todo o vídeo de entrada. Se **rcTarget** estiver vazio, o filtro A preencherá todo o buffer de saída.

Por exemplo, suponha que o filtro A está recebendo dados de vídeo de 160 x 120 pixels. Suponha também que o filtro A esteja conectado ao filtro B com o tipo de mídia a seguir.

-   (**biWidth**, **biHeight**): 320, 240
-   **rcSource**: (0, 0, 0, 0)
-   **rcTarget:**(0, 0, 0, 0)

Isso significa que o filtro A ampliará o vídeo recebido por 2 nas direções x e y e preencherá um buffer de saída de 320 x 240.

Como outro exemplo, suponha que o filtro A esteja recebendo dados de vídeo de 160 x 120 e que ele esteja conectado ao filtro B com o tipo de mídia a seguir.

-   (**biWidth**, **biHeight**): 320, 240
-   **rcSource:**(0, 0, 160, 240)
-   **rcTarget:**(0, 0, 0, 0)

O **membro rcSource** é relativo ao tamanho do buffer conectado de 320, 240. Porque o **rcSource especificado** (0, 0, 160, 240) é a metade esquerda do buffer, o filtro A pegará a metade esquerda de seu vídeo de entrada ou a parte (0, 0, 80, 120) e ampliará o vídeo para um tamanho de (320, 240) (por 4 na direção x e por 2 na direção y) e preenchendo o buffer de saída 320 x 240.

Agora suponha que o filtro A chama [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md)e o exemplo de mídia retornado tem um tipo de mídia anexado a ele, o que significa que o filtro B deseja que o filtro A forneça um tamanho ou tipo de vídeo diferente do que ele forneceu anteriormente. Suponha que o novo tipo de mídia seja:

-   (**biWidth**, **biHeight**): 640, 480
-   **rcSource:**(0, 0, 160, 120)
-   **rcTarget:**(0, 0, 80, 60)

Isso significa que o exemplo de mídia tem um buffer de 640 x 480 de tamanho. O membro **rcSource** é relativo ao tipo de mídia conectado original (320, 240) e não ao novo tipo de mídia de (640, 480), **portanto, rcSource** especifica que o canto superior esquerdo (25%) do vídeo de entrada deve ser usado. Essa parte do vídeo de entrada é colocada nos pixels superior esquerdo (80, 60) do buffer de saída 640 x 480, conforme especificado por **rcTarget** de (0, 0, 80, 60). Como o filtro A está recebendo vídeo de 160 x 120, o canto superior esquerdo do vídeo de entrada é uma peça (80, 60), o mesmo tamanho do bitmap de saída e nenhum alongamento é necessário.

O filtro A não colocará dados nos outros pixels do buffer de saída e deixará esses bits inalterados. O **membro rcSource** é limitado pelo **biWidth** e **pelo biHeight** do tipo de mídia conectada original entre os filtros A e B, e **rcTarget** é limitado pelos novos **biWidth** e **biHeight** do exemplo de mídia. No exemplo anterior, **rcSource** não pôde sair dos limites de (0, 0, 320, 240) e **rcTarget** não pôde sair dos limites de (0, 0, 640, 480).

 

 



