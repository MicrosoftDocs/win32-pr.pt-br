---
description: Os tipos de contador de algoritmos de contador podem calcular taxas ou médias de bytes para uma amostra ou ao longo de um período de tempo para uma operação específica.
ms.assetid: 4423e35e-2a93-4f68-8494-89df05268cc9
ms.tgt_platform: multiple
title: Tipos de contadores de algoritmo de contador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5568d4df0d1b50fd55a4f9d007d6506cf59a8f67a05885c21d64a6be8812536c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131428"
---
# <a name="counter-algorithm-counter-types"></a>Tipos de contadores de algoritmo de contador

Os tipos de contador de algoritmos de contador podem calcular taxas ou médias de bytes para uma amostra ou ao longo de um período de tempo para uma operação específica.

A propriedade **AvgDiskBytesPerTransfer** na classe [**de \_ PhysicalDisk do PerfRawData de \_ perfdisk \_ do Win32**](/previous-versions//aa394308(v=vs.85)) usa o tipo de número de \_ massa médio de perf \_ . Nesse caso, a transferência é a operação e o número acumulado de bytes que são enviados são os dados do contador. Para quaisquer dois exemplos, dividir a diferença de bytes acumulados pela diferença em acumular transferências produzirá o número médio de bytes por transferência durante o período entre os exemplos.

Os seguintes algoritmos de contador são fornecidos:



| CounterType                                                                                              | Descrição                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Desempenho \_ MÉDIA decimal \_ em massa](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1073874176<br/>       | Número de itens processados, em média, durante uma operação. Esse tipo de contador exibe uma taxa dos itens processados (como bytes enviados) para o número de operações concluídas e requer uma propriedade base com a \_ \_ base média de perf como o tipo de contador. |
| [Desempenho \_ \_Contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))de contadores decimal 272696320<br/>     | Número médio de operações concluídas durante cada segundo do intervalo de amostragem. .                                                                                                                                                                          |
| [Desempenho \_ \_Contador de exemplo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 4260864<br/>        | Número médio de operações concluídas em um segundo. Esse tipo de contador requer uma propriedade base com o tipo de contador \_ base de exemplo perf \_ .                                                                                                                   |
| [Desempenho \_ \_ \_ Contagem de massa de contadores](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 272696576<br/> | Número médio de operações concluídas durante cada segundo do intervalo de amostragem. Esse tipo de contador é o mesmo que o \_ tipo de contador de contador de desempenho \_ , mas usa campos maiores para acomodar valores maiores.                                                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de contador de desempenho WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

