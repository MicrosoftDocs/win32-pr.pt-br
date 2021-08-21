---
description: Objetos de linha do tempo
ms.assetid: da426964-d5bd-45ca-a914-c19062f3564b
title: Objetos de linha do tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbcf3496770dee7664e08ffabe6537356c7b37ad13abee1dce149698748745e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072300"
---
# <a name="timeline-objects"></a>Objetos de linha do tempo

\[Essa API não tem suporte e pode ser alterada ou não disponível no futuro.\]

Cada tipo de objeto na linha do tempo – origem, faixa, efeito e assim por diante – é um objeto COM distinto. No entanto, um aplicativo não os cria usando a **função CoCreateInstance.** Em vez disso, ele chama [**o método IAMTimeline::CreateEmptyNode.**](iamtimeline-createemptynode.md) Esse método cria um objeto do tipo solicitado, inicializa-o e retorna um ponteiro para o objeto . Para obter detalhes, consulte [Construindo uma linha do tempo.](constructing-a-timeline.md)

Cada objeto de linha do tempo expõe a interface [**IAMTimelineObj.**](iamtimelineobj.md) Além disso, os vários tipos de objeto suportam suas próprias interfaces especializadas:

-   Origem: [ **IAMTimelineSrc**](iamtimelinesrc.md)
-   Faixa: [ **IAMTimelineTrack**](iamtimelinetrack.md)
-   Composição: [ **IAMTimelineComp**](iamtimelinecomp.md)
-   Grupo: [**IAMTimelineComp,**](iamtimelinecomp.md) [**IAMTimelineGroup**](iamtimelinegroup.md)
-   Efeito: [ **IAMTimelineEffect**](iamtimelineeffect.md)
-   Transição: [ **IAMTimelineTrans**](iamtimelinetrans.md)

Observe que os grupos são um tipo de composição, portanto, eles suportam [**IAMTimelineComp**](iamtimelinecomp.md), bem como sua própria interface [**IAMTimelineGroup.**](iamtimelinegroup.md)

Além das interfaces listadas anteriormente, os objetos de linha do tempo expõem outras interfaces secundárias. Essas interfaces determinam as relações entre os tipos de objeto.



| Interface                                                  | Significado                                                                                                       | Exposto por                        |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | O objeto é uma faixa virtual. As faixas virtuais podem residir dentro de composições e manter outros objetos de linha do tempo. | Composição, Faixa                |
| [**IAMTimelineEffectable**](iamtimelineeffectable.md)     | O objeto pode ter efeitos.                                                                                  | Composição, Faixa, Origem        |
| [**IAMTimelineTransable**](iamtimelinetransable.md)       | O objeto pode ter transições.                                                                              | Composição, Faixa                |
| [**IAMTimelineSplittable**](iamtimelinesplittable.md)     | O objeto pode ser dividido em dois objetos.                                                                     | Track, Source, Effect, Transition |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral dos componentes da linha do tempo](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



