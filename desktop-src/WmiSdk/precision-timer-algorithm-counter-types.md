---
description: Os tipos de contadores do algoritmo de timer de precisão obtêm leituras mais precisas do que os temporizadores do sistema.
ms.assetid: f7159645-6287-47a3-895e-20dae6e0892a
ms.tgt_platform: multiple
title: Tipos de contadores de algoritmo de timer de precisão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a8864587fedc915678dfa4a9e578ca051e1262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663245"
---
# <a name="precision-timer-algorithm-counter-types"></a>Tipos de contadores de algoritmo de timer de precisão

Os tipos de contadores do algoritmo de timer de precisão obtêm leituras mais precisas do que os temporizadores do sistema. O serviço que fornece os dados também fornece um carimbo de data/hora, que elimina os erros que podem ocorrer devido ao tempo pequeno e variável que decorre entre a captura do carimbo de data/hora do sistema e a coleta dos dados da DLL de desempenho. Esse carimbo de data/hora base para temporizadores de precisão é uma \_ propriedade de carimbo de data/hora de precisão de desempenho \_ , que deve seguir imediatamente a \_ \_ Propriedade temporizador



| Constante de tipo                                                                                         | Descrição                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Desempenho \_ \_ \_ Temporizador do sistema de precisão](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 541525248<br/> | Semelhante ao timer do contador de desempenho \_ \_ , exceto que ele usa uma base de tempo definida do contador em vez do carimbo de data/hora do sistema.             |
| [Desempenho \_ PRECISÃO de \_ 100 NS do \_ temporizador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 542573824<br/>  | Semelhante ao \_ \_ temporizador perf 100NSEC, exceto pelo fato de que ele usa uma base de tempo definida do contador de 100 NS em vez do carimbo de data/hora de 100 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de contador de desempenho WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

