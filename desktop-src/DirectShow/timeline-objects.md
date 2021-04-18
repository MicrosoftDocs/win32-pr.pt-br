---
description: Objetos de linha do tempo
ms.assetid: da426964-d5bd-45ca-a914-c19062f3564b
title: Objetos de linha do tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580286b31afd77f064411dd29d60a62b80bfb51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750873"
---
# <a name="timeline-objects"></a>Objetos de linha do tempo

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Cada tipo de objeto na linha do tempo — origem, controle, efeito e assim por diante — é um objeto COM distinto. No entanto, um aplicativo não os cria usando a função **CoCreateInstance** . Em vez disso, ele chama o método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) . Esse método cria um objeto do tipo solicitado, inicializa-o e retorna um ponteiro para o objeto. Para obter detalhes, consulte [construindo uma linha do tempo](constructing-a-timeline.md).

Cada objeto Timeline expõe a interface [**IAMTimelineObj**](iamtimelineobj.md) . Além disso, os vários tipos de objeto dão suporte a suas próprias interfaces especializadas:

-   Origem: [ **IAMTimelineSrc**](iamtimelinesrc.md)
-   Controle: [ **IAMTimelineTrack**](iamtimelinetrack.md)
-   Composição: [ **IAMTimelineComp**](iamtimelinecomp.md)
-   Grupo: [**IAMTimelineComp**](iamtimelinecomp.md), [**IAMTimelineGroup**](iamtimelinegroup.md)
-   Efeito: [ **IAMTimelineEffect**](iamtimelineeffect.md)
-   Transição: [ **IAMTimelineTrans**](iamtimelinetrans.md)

Observe que os grupos são um tipo de composição, portanto, dão suporte a [**IAMTimelineComp**](iamtimelinecomp.md), bem como sua própria interface [**IAMTimelineGroup**](iamtimelinegroup.md) .

Além das interfaces listadas anteriormente, os objetos de linha do tempo expõem outras interfaces secundárias. Essas interfaces determinam as relações entre os tipos de objeto.



| Interface                                                  | Significado                                                                                                       | Exposto por                        |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | O objeto é uma faixa virtual. As faixas virtuais podem residir em composições e conter outros objetos de linha do tempo. | Composição, faixa                |
| [**IAMTimelineEffectable**](iamtimelineeffectable.md)     | O objeto pode ter efeitos.                                                                                  | Composição, faixa, origem        |
| [**IAMTimelineTransable**](iamtimelinetransable.md)       | O objeto pode ter transições.                                                                              | Composição, faixa                |
| [**IAMTimelineSplittable**](iamtimelinesplittable.md)     | O objeto pode ser dividido em dois objetos.                                                                     | Rastrear, origem, efeito, transição |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral dos componentes da linha do tempo](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



