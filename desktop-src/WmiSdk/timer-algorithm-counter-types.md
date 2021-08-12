---
description: Os tipos de contador de algoritmos de temporizador são baseados na quantidade de uso maior do objeto de desempenho em um período de exemplo.
ms.assetid: 4ec49efc-2b0f-4205-8b58-fb121da32b4e
ms.tgt_platform: multiple
title: Tipos de contadores de algoritmo de temporizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e3a606babb005eca7f01f75f735cd6d6a9da29c9c1427c56614c318f9465f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554010"
---
# <a name="timer-algorithm-counter-types"></a>Tipos de contadores de algoritmo de temporizador

Os tipos de contador de algoritmos de temporizador são baseados na quantidade de uso maior do objeto de desempenho em um período de exemplo. Os dados do contador são uma medida de Quantum crescente da atividade total de um objeto até o momento em que o exemplo ocorre. A diferença entre os dois exemplos indica o tempo total em que o objeto está ativo durante o período de tempo de exemplo.

Dividir pelo período de exemplo resulta em uma proporção de tempo em que o objeto está ativo durante um período de tempo. Dividir pelo número de interrupções de sondagem interna determina o uso médio entre amostras de sondagem.

Por exemplo, a propriedade **AvgDiskSecPerRead** na classe [**de \_ PhysicalDisk do PerfRawData do Win32 \_ perfdisk \_**](/previous-versions//aa394308(v=vs.85)) usa o tipo de contador de tempo **\_ médio \_ de perf** . Ele calcula o tempo médio em segundos de uma leitura de dados do disco e requer a propriedade base **AvgDiskSecPerRead \_ base**. Ao contrário do **\_ \_ Timer do contador de desempenho**, a base do temporizador médio representa um número acumulado de operações e os dados do contador são um valor de tempo de execução, o que significa que, quando dividido pela base de tempo, ele gera o tempo total de todas as operações em segundos.



| Constante de tipo de contador                                                                                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_Timer do contador de desempenho \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 541132032<br/>             | Tempo médio que um componente está ativo como uma porcentagem do tempo de amostragem total.<br/>                                                                                                                                                                                                                                                                                                         |
| [Timer do contador de desempenho \_ \_ \_ inv](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 557909248<br/>        | Percentual médio de tempo observado durante o intervalo de amostragem em que o objeto não está ativo. Esse tipo de contador é o mesmo que o **perf \_ 100NSEC \_ timer \_ inv** , exceto pelo fato de que ele mede o tempo em unidades de tiques do timer de desempenho do sistema em vez de em unidades de 100ns.<br/>                                                                                                                       |
| [\_temporizador de média de desempenho \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 805438464<br/>             | Tempo médio para concluir um processo ou uma operação. Esse tipo de contador exibe uma taxa do tempo total decorrido do intervalo de exemplo para o número de processos ou operações concluídas durante esse tempo.<br/> Esse tipo de contador requer uma propriedade base **com \_ \_ base de desempenho médio** como o tipo de contador.<br/>                                                                         |
| [\_ \_ Temporizador 100NSEC perf](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 542180608<br/>             | Tempo ativo de um componente como um percentual do tempo total decorrido em unidades de 100 NS do intervalo de amostragem.<br/>                                                                                                                                                                                                                                                                          |
| [\_Contador de \_ temporizador 100NSEC de desempenho \_ inv](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 558957824<br/>        | Porcentagem de tempo em que o objeto não estava em uso. Esse tipo de contador é o mesmo que o **contador de desempenho \_ \_ timer \_ inv** , exceto pelo fato de que ele mede o tempo em unidades de 100ns em vez de em tiques do timer de desempenho do sistema.<br/>                                                                                                                                                                                   |
| [\_ \_ múltiplo Timer do contador de desempenho \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 574686464<br/>      | Tempo ativo de um ou mais componentes como uma porcentagem do tempo total do intervalo de amostragem. Esse tipo de contador difere do **perf \_ 100NSEC \_ multi \_ timer** , pois ele mede o tempo em unidades de tiques do temporizador de desempenho do sistema, em vez de em unidades de 100ns.<br/> Esse tipo de contador requer uma propriedade base com o tipo de contador de **\_ \_ \_ base múltiplo do contador de desempenho** .<br/>        |
| [\_ \_ multi timer de \_ contador de desempenho \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 591463680<br/> | Tempo inativo de um ou mais componentes como uma porcentagem do tempo total do intervalo de amostragem. Esse tipo de contador é diferente de **perf \_ 100NSEC \_ multi \_ timer \_ inv** , pois ele mede o tempo em unidades de tiques do temporizador de desempenho do sistema, em vez de em unidades de 100ns.<br/> Esse tipo de contador requer uma propriedade base com o tipo de contador de **\_ \_ \_ base múltiplo do contador de desempenho** .<br/> |
| [\_Timer de \_ vários \_ 100NSEC perf](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 575735040<br/>      | Esse tipo de contador mostra o tempo ativo de um ou mais componentes como uma porcentagem do tempo total (100ns unidades) do intervalo de amostragem.<br/> Esse tipo de contador requer uma propriedade base com o tipo de contador de **\_ \_ \_ base múltiplo do contador de desempenho** .<br/>                                                                                                                                     |
| [PERF \_ 100NSEC \_ multi \_ timer \_ inv](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 592512256<br/> | Tempo inativo de um ou mais componentes como uma porcentagem do tempo total do intervalo de amostragem. Contadores desse tipo de tempo de medida em unidades de 100ns.<br/> Esse tipo de contador requer uma propriedade base com o tipo de contador de **\_ \_ \_ base múltiplo do contador de desempenho** .<br/>                                                                                                                          |
| [\_ \_ temporizador de tempo de obj perf \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))<br/> Decimal 543229184<br/>           | Um temporizador de 64 bits em unidades específicas do objeto.<br/>                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de contador de desempenho WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

