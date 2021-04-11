---
description: Depois de criar uma consulta e adicionar contadores a ela, chame a função PdhCollectQueryData para recuperar os dados brutos atuais de todos os contadores na consulta.
ms.assetid: 2534d387-a280-4716-9a9d-3e42f40e2f92
title: Coletando dados de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99bd2c0e22553245e87d3844694051c88c57895
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296753"
---
# <a name="collecting-performance-data"></a>Coletando dados de desempenho

Depois de [criar uma consulta](creating-a-query.md) e adicionar contadores a ela, chame a função [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) para recuperar os dados brutos atuais de todos os contadores na consulta.

Muitos contadores, como contadores de taxa, exigem dois exemplos de dados para calcular um valor de dados formatado. A PDH mantém dados para o exemplo atual e o exemplo coletado anteriormente. O procedimento a seguir descreve como coletar valores de contador que exigem dois exemplos para calcular um valor de exibição.

**Para coletar valores de contador que exigem dois exemplos para calcular um valor de exibição**

1.  Chame [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) para coletar a primeira amostra.
2.  Chame a função [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) para aguardar um mínimo de um segundo entre coleções.
3.  Chame [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) novamente para coletar a segunda amostra.
4.  Chame a função [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue) para calcular um valor de exibição.
5.  Repita as etapas de 2 a 4.

Como uma alternativa para implementar um período de espera por conta própria, você pode chamar a função [**PdhCollectQueryDataEx**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydataex) , que cria um thread de tempo que aguarda um período de tempo especificado, coleta o exemplo e dispara um evento definido pelo aplicativo.

Se você quiser consultar dados de desempenho de um arquivo de log, também poderá definir um intervalo de tempo. O intervalo de tempo limita a consulta a esses exemplos que foram coletados dentro do intervalo de tempo (cada exemplo contém um carimbo de data/hora para quando ele foi coletado). Para obter mais informações sobre como definir e recuperar intervalos de tempo, consulte [definindo um intervalo de tempo para uma consulta](setting-a-time-range-for-a-query.md).

Se você quiser coletar dados de desempenho e gravá-los em um arquivo de log, chame a função [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga) em vez de chamar [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata). Para obter detalhes, consulte [trabalhando com arquivos de log](working-with-log-files.md) e [gravando dados de desempenho em um arquivo de log](writing-performance-data-to-a-log-file.md).

Para obter detalhes sobre como calcular um valor de amostra exibível, consulte [exibindo dados de desempenho](displaying-performance-data.md).

## <a name="understanding-multiple-processor-counters"></a>Compreendendo vários contadores de processador

Alguns contadores de desempenho foram projetados para sistemas de processador único e podem não ser precisos para computadores com vários processadores. Por exemplo, um processo é limitado a 100% de um único processador; no entanto, seus threads podem usar vários processadores, totalizando mais de 100%.

O \\ valor do contador "processador ( \_ total) \\ % tempo do processador" é o uso médio de todos os processadores. Por exemplo, se você tiver dois processadores, um a 100 por cento e outro em 0%, este contador relatará 50%. Portanto, o intervalo é de 0 a 100.

O \\ valor do contador "processar (X) \\ % tempo de processamento" é a soma do uso do processador por todos os threads do processo X. Por exemplo, em um computador com dois processadores, se um processo tiver dois threads, um que ocupa 75% de uma CPU e o outro, com 80% de outra CPU, esse contador relatará 155%. O intervalo para esse contador é de 0 a 100 \* ProcessorCount.

* * Windows Server 2003 e Windows XP: * *

Você pode receber valores fora do intervalo de valores esperado para uso da CPU. Para calcular a porcentagem de uso da CPU, a PDH precisa de dois exemplos (cada um com um valor bruto e um carimbo de data/hora). Como a PDH usa apenas o nome da instância para corresponder aos processos, às vezes ele pode usar dois exemplos de processos diferentes. Por exemplo, se três processos estiverem sendo amostrados e um processo for encerrado após o terceiro exemplo, outro processo será movido para o slot vagado por esse processo encerrado. Como resultado, um contador formatado fornecerá um valor incorreto quando você formatar o quarto exemplo, pois ele está usando o terceiro exemplo do processo encerrado e o quarto exemplo do processo que foi movido para o slot do processo encerrado.

A tabela a seguir mostra como isso pode ocorrer se um processo for encerrado enquanto os dados estão sendo coletados. A tabela mostra cinco exemplos de valor de contador para três instâncias do processo X. Os exemplos são coletados em intervalos de um segundo. Depois que o terceiro exemplo for coletado, o processo X no slot 1 será encerrado. Quando o processo X no slot 1 é encerrado, o processo X no slot 2 muda para o slot 1. Quando você coleta a quarta amostra para o processo X no slot 2, o primeiro valor é agora 20 em vez de 1.000, e o segundo valor é 1.500. Ao Formatar o valor do contador, você obtém 1.480 milissegundos em vez dos 500 milissegundos esperados. Ao Formatar o quinto valor de exemplo, você deve obter o valor esperado.

| Amostra   | Slot 0 para o processo X | Slot 1 para o processo X           | Slot 2 para o processo X                     |
|----------|----------------------|--------------------------------|------------------------------------------|
| Exemplo 1 | 0                    | 0                              | 0                                        |
| Exemplo 2 | 20                   | 10                             | 500                                      |
| Exemplo 3 | 40                   | 20                             | 1,000                                    |
| Exemplo 4 | 60                   | 1.500 (do slot anterior 2) | Não aplicável. Coletado agora no slot 1. |
| Exemplo 5 | 80                   | 2\.000                          | Não aplicável. Coletado agora no slot 1. |



 

 

 
