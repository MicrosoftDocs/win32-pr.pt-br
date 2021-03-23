---
title: Contadores, consultas e predicação
description: Os contadores de saída de fluxo e UAV operam no Direct3D 12 em um método semelhante ao Direct3D 11, embora agora a memória para os contadores deva ser alocada pelo aplicativo, o driver não o faz.
ms.assetid: 8BDDAFEF-57D4-4EF5-BB0C-6C96AF557A45
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314c01b05ac31e5d5f8348b775c8955ae382f5ed
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104548306"
---
# <a name="counters-queries-and-predication"></a>Contadores, consultas e predicação

Este tópico aborda contadores de saída de fluxo, contadores de UAV, consultas e predicação.

Os contadores de saída de fluxo e UAV operam no Direct3D 12 em um método semelhante ao Direct3D 11, embora agora a memória para os contadores deva ser alocada pelo aplicativo, o driver não o faz. As consultas no Direct3D 12 são mais diferentes das do Direct3D 11, com a adição de limites e outros processos que eliminam a necessidade de alguns tipos de consulta.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                           | Descrição                                                                                                                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Contadores de saída de fluxo](stream-output-counters.md)<br/> | A saída de fluxo é a capacidade da GPU de gravar vértices em um buffer. Os contadores de saída do fluxo monitoram o progresso.<br/>                                                               |
| [Contadores de UAV](uav-counters.md)<br/>                     | Os contadores UAV podem ser usados para associar um contador atômico de 32 bits a um UAV (unordened-Access-View).<br/>                                                                                |
| [Consultas](queries.md)<br/>                               | No Direct3D 12, as consultas são agrupadas em matrizes de consultas chamadas de heap de consulta. Um heap de consulta tem um tipo que define os tipos válidos de consultas que podem ser usadas com esse heap.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Medição de desempenho](performance-measurement.md)
</dt> </dl>

 

 





