---
description: Sobre a renderização de vídeo no DirectShow
ms.assetid: 3b064758-2ae5-4441-801c-5400e4ef3790
title: Sobre a renderização de vídeo no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699e8ecf133f362e699e6b9d650d11da5bf43347
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825995"
---
# <a name="about-video-rendering-in-directshow"></a>Sobre a renderização de vídeo no DirectShow

O DirectShow fornece vários filtros que renderizam vídeo:

-   Filtro de [renderização de vídeo](video-renderer-filter.md) . Esse filtro está disponível para todas as plataformas que dão suporte ao DirectX e não tem nenhum requisito de sistema específico. O processador de vídeo usa o DirectDraw sempre que possível para renderizar o vídeo; caso contrário, ele usa GDI. Esse filtro é o processador de vídeo padrão nas plataformas anteriores ao Windows XP.
-   [Filtro de processador de mixagem de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7). O VMR-7 está disponível no Windows XP, onde é o processador de vídeo padrão. O VMR-7 sempre usa o DirectDraw 7 para renderização. Ele fornece muitos recursos avançados não disponíveis no filtro de processamento de vídeo mais antigo, incluindo um modelo de plug-in onde o aplicativo controla as superfícies do DirectDraw usadas para renderização.
-   [Filtro de processador de mixagem de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9). O VMR-9 é uma versão mais recente do processador de mixagem de vídeo que usa o Direct3D 9 para renderização. Ele está disponível para todas as plataformas que dão suporte ao DirectX. No entanto, ele não é o renderizador padrão porque tem requisitos de sistema maiores do que o filtro de processador de vídeo.
-   O filtro de [mixer de sobreposição](overlay-mixer-filter.md) foi projetado especificamente para reprodução de DVD e vídeo de difusão. Ele também dá suporte a VPEs (extensões de porta de vídeo), permitindo que ele funcione com decodificadores de hardware MPEG-2 ou sintonizadores de TV analógicos que enviam vídeos diretamente para a placa gráfica.
-   O filtro EVR ( [**processador de vídeo avançado**](enhanced-video-renderer-filter.md) ) está disponível a partir do Windows Vista. Ele oferece melhor desempenho de vídeo em comparação com os renderizadores de vídeo anteriores, especialmente quando a composição do Windows Vista Desktop está habilitada.

Em geral, o EVR é preferido para aplicativos direcionados para o Windows Vista ou posterior, e o VMR-9 é preferido para aplicativos executados em versões anteriores do Windows. Para obter mais informações sobre como usar os filtros do VMR-7 e do VMR-9, consulte [usando o processador de mixagem de vídeo](using-the-video-mixing-renderer.md).

Modo em janela e modo sem janela

Um processador de vídeo do DirectShow pode operar em modo de *janela* ou *sem janela* .

-   No modo de janela, o renderizador cria sua própria janela para exibir o vídeo. Normalmente, você tornará essa janela o filho de uma janela de aplicativo. Para obter mais informações, consulte [usando o modo de janela](using-windowed-mode.md).
-   No modo sem janela, o renderizador desenha o vídeo diretamente em uma janela de aplicativo. Ele não cria sua própria janela. Para obter mais informações sobre esse modo, consulte [usando o modo sem janela](using-windowless-mode.md).

O filtro de processador de vídeo dá suporte apenas ao modo de janela. Os filtros VMR-7 e VMR-9 dão suporte a ambos os modos. Eles assumem como padrão o modo em janela para compatibilidade com versões anteriores, mas o modo sem janela é preferencial. O EVR dá suporte apenas ao modo sem janela.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização de vídeo](video-rendering.md)
</dt> </dl>

 

 



