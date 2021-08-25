---
description: Modos de operação do VMR
ms.assetid: 98244af1-5934-4d1c-b9c3-7a414b065fe7
title: Modos de operação do VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88e7a1fa378ff781a712f71c877c32991cf19683a81daa10ff9b2fbbea40e7c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049366"
---
# <a name="vmr-modes-of-operation"></a>Modos de operação do VMR

A arquitetura do componente do VMR permite que os aplicativos o configurem de várias maneiras, dependendo de como a renderização deve ser executada. A tabela a seguir mostra os três modos de apresentação e os dois modos de combinação e os componentes que estão presentes para cada configuração.



| Mode       | Fluxo único                                                                     | vários Fluxos (modo de combinação)                                                                                             |
|------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Em janelas   | Alocador-unidade de sincronização presenterCore<br/> Gerenciador de janelas<br/> | MixerCompositor\*<br/> Alocador-apresentador<br/> Unidade de sincronização principal<br/> Gerenciador de janelas<br/> |
| Sem janelas | Alocador-unidade de sincronização presenterCore<br/>                           | MixerCompositor\*<br/> Alocador-apresentador<br/> Unidade de sincronização principal<br/>                           |
| Com renderização | Unidade de sincronização de núcleo de alocador (fornecido pela aplicação)<br/> | MixerCompositor\*<br/> Alocador-Presenter (fornecido pelo aplicativo)<br/> Unidade de sincronização principal<br/> |



 

\* Indica que o aplicativo tem a opção de fornecer um componente personalizado ou usar o componente padrão.

Em todas as configurações, o ponto principal a ser lembrado quando você cria gráficos de filtro com o VMR é que você deve configurar o VMR antes de conectá-lo.

Para todas as configurações, os Pins não podem ser adicionados ou removidos dinamicamente depois que o VMR está conectado ao filtro upstream, mas eles podem ser conectados e desconectados. Se o aplicativo não tiver certeza de quantos Pins serão necessários, ele deverá configurar o VMR para o número máximo que pode ser necessário. A presença de Pins de entrada não utilizados no filtro não degrada o desempenho de renderização. ao contrário da sobreposição antiga Mixer, o VMR não tem nenhum pino de saída porque não requer um filtro separado para o gerenciamento de janelas.

As seções a seguir descrevem como configurar o VMR para um determinado modo:

-   [Modo de janela do VMR (compatibilidade)](vmr-windowed--compatibility--mode.md)
-   [Modo sem janela do VMR](vmr-windowless-mode.md)
-   [VMR com vários Fluxos (modo de combinação)](vmr-with-multiple-streams--mixing-mode.md)
-   [Modo de mixagem YUV](yuv-mixing-mode.md)
-   [Posicionando e movendo os retângulos de vídeo no espaço de composição](positioning-and-moving-video-rectangles-in-composition-space.md)
-   [Modo de reprodução do VMR (alocador personalizado-apresentadores)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
-   [Modo exclusivo do DirectDraw](directdraw-exclusive-mode.md)

 

 




