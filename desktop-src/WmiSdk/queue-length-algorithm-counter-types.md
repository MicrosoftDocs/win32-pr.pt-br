---
description: Os tipos de contadores de algoritmo de comprimento de fila incrementam o número de itens em uma fila em cada intervalo de amostragem, conforme especificado pela propriedade Frequency apropriada&\# 8212; Frequência \_ PerfTime e assim por diante.
ms.assetid: 514b1a79-ed9d-4ec6-a6ea-b3490291ce18
ms.tgt_platform: multiple
title: Tipos de contadores de algoritmo de comprimento de fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9fd3019e9a5e7150402266fd206d3f460f3d0ae3b07f4c6c7d51e82473e9dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316533"
---
# <a name="queue-length-algorithm-counter-types"></a>Tipos de contadores de algoritmo de comprimento de fila

Os tipos de contadores de algoritmo de comprimento de fila incrementam o número de itens em uma fila em cada intervalo de amostragem, conforme especificado pela frequência de propriedade de frequência apropriada \_ e assim por diante. O resultado de cooked divide pelo número de amostras para produzir o comprimento médio da fila.

Um exemplo é a propriedade **AvgDiskQueueLength** no [**\_ LogicalDisk do PerfRawData de \_ perfdisk \_ do Win32**](./retrieving-raw-and-formatted-performance-data.md) que usa o tipo de contador contador de desempenho de \_ \_ 100 NS \_ QUEUELEN \_ tipo.



| Constante de tipo                                                                                                 | Descrição                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Desempenho \_ COUNTER \_ QUEUELEN \_ tipo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 4523008<br/>            | Duração média de uma fila para um recurso ao longo do tempo. Ele mostra a diferença entre os tamanhos de fila observados durante os últimos dois intervalos de amostragem divididos pela duração do intervalo.                       |
| [Desempenho \_ COUNTER \_ grande \_ QUEUELEN \_ tipo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 4523264<br/>     | Duração média de uma fila para um recurso ao longo do tempo. Contadores desse tipo mostram a diferença entre os tamanhos de fila observados durante os últimos dois intervalos de amostragem divididos pela duração do intervalo. |
| [Desempenho \_ COUNTER \_ 100ns \_ QUEUELEN \_ tipo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 5571840<br/>     | Duração média de uma fila para um recurso ao longo do tempo em unidades de 100 nanossegundos.                                                                                                                                        |
| [Desempenho \_ \_Tipo de \_ \_ QUEUELEN \_ de tempo de OBJ de contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 6620416<br/> | Hora em que um objeto está em uma fila.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de contador de desempenho WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

