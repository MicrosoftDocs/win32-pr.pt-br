---
description: Criando composições e faixas de grupos
ms.assetid: c3bef3cd-5e3c-42c5-850f-b4cb00c414bd
title: Criando composições e faixas de grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2808c2d096b52ad73da7d518d703bc25103751d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103826020"
---
# <a name="creating-groups-compositions-and-tracks"></a>Criando composições e faixas de grupos

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Grupos, composições e faixas são as camadas intermediárias entre a linha do tempo e os clipes de origem. Elas são diferenciadas pelo tipo de objeto que podem conter.

-   As faixas contêm objetos de origem.
-   As composições contêm faixas e outras composições, mas não objetos de origem.
-   Os grupos são as composições de nível superior. Os grupos contêm composições e faixas, mas as composições não podem conter grupos.
-   Um *controle virtual* é qualquer objeto que possa residir dentro de uma composição ou um grupo. Isso inclui faixas e composições.

Esses objetos expõem as seguintes interfaces:



| Interface                                                  | Exposto por           |
|------------------------------------------------------------|----------------------|
| [**IAMTimelineTrack**](iamtimelinetrack.md)               | Faixas               |
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | Faixas, composições |
| [**IAMTimelineComp**](iamtimelinecomp.md)                 | Composições, grupos |
| [**IAMTimelineGroup**](iamtimelinegroup.md)               | Grupos               |



 

Essas interfaces contêm os métodos para adicionar objetos à linha do tempo.

-   [**IAMTimeline:: addgroup**](iamtimeline-addgroup.md): insere um grupo na linha do tempo.
-   [**IAMTimelineComp:: VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md): insere uma faixa virtual em uma composição ou grupo.
-   [**IAMTimelineTrack:: SrcAdd**](iamtimelinetrack-srcadd.md): insere uma fonte em um controle.

Por exemplo, o código a seguir insere uma nova faixa em um grupo. Conforme mostrado na tabela anterior, um grupo é considerado um tipo de composição, e uma faixa é um tipo de faixa virtual. Portanto, para inserir a faixa no grupo, você deve consultar o grupo para sua interface **IAMTimelineComp** e chamar o método **IAMTimelineComp:: VTrackInsBefore** .


```C++
IAMTimelineGroup    *pGroup;
// Create a new group (not shown). 

IAMTimelineComp     *pComp = NULL;
IAMTimelineObj      *pTrackObj = NULL;

pTL->CreateEmptyNode(&pTrackObj, TIMELINE_MAJOR_TYPE_TRACK);
pGroup->QueryInterface(IID_IAMTimelineComp, (void **)&pComp);
pComp->VTrackInsBefore(pTrackObj, 0);
```



O segundo parâmetro para **VTrackInsBefore** especifica a prioridade da faixa virtual. Os níveis de prioridade começam em zero. Se você especificar o valor – 1, a faixa virtual será inserida no final da lista de prioridades. Se você especificar um valor onde já exista uma faixa virtual, tudo desse ponto em será movido para baixo na lista por um nível de prioridade. Não insira uma faixa virtual em uma prioridade maior que o número de faixas virtuais, pois isso causará um comportamento indefinido.

Para excluir um objeto permanentemente da linha do tempo, chame [**IAMTimelineObj:: RemoveAll**](iamtimelineobj-removeall.md) no objeto. Esse método remove o objeto e todos os seus filhos. Para remover um objeto com a finalidade de reinseri-lo em outro lugar na linha do tempo, chame [**IAMTimelineObj:: Remove**](iamtimelineobj-remove.md) em vez disso. Ao contrário de **RemoveAll**, esse método não exclui os filhos do objeto. Para remover tudo da linha do tempo, chame [**IAMTimeline:: ClearAllGroups**](iamtimeline-clearallgroups.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Construindo uma linha do tempo](constructing-a-timeline.md)
</dt> </dl>

 

 



