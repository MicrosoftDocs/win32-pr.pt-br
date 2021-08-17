---
description: Os tipos de contador de algoritmo de temporizador de precisão obtém leituras mais precisas do que os temporizadores do sistema.
ms.assetid: f7159645-6287-47a3-895e-20dae6e0892a
ms.tgt_platform: multiple
title: Tipos de contador de algoritmo de temporizador de precisão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 137d136db0b4dd579dfec4673b09ce216bef4042d9356b3938b79e7817e3d83a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131028"
---
# <a name="precision-timer-algorithm-counter-types"></a>Tipos de contador de algoritmo de temporizador de precisão

Os tipos de contador de algoritmo de temporizador de precisão obtém leituras mais precisas do que os temporizadores do sistema. O serviço que fornece os dados também fornece um timestamp, que elimina os erros que podem ocorrer devido ao tempo pequeno e variável que ocorre entre a captura do timestamp do sistema e a coleta dos dados da DLL de desempenho. Esse data/hora base para temporizadores de precisão é uma propriedade TIMESTAMP DE PRECISÃO PERF, que deve seguir imediatamente a \_ \_ propriedade TIMER DE PRECISÃO PERF. \_ \_



| Constante CounterType                                                                                         | Descrição                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [PERF \_ Precisão \_ do \_ TEMPORIZADOR DO SISTEMA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimais 541525248<br/> | Semelhante a PERF COUNTER TIMER, exceto que ele usa uma base de tempo definida pelo \_ contador em vez do \_ timestamp do sistema.             |
| [PERF \_ PRECISÃO \_ 100NS \_ TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 542573824<br/>  | Semelhante ao TEMPORIZADOR PERF 100NSEC, exceto que ele usa uma base de tempo definida pelo contador de 100ns em vez do \_ \_ timestamp de 100ns do sistema. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de contador de desempenho WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

