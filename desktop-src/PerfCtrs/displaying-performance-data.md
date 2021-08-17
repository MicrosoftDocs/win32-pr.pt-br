---
description: A maioria dos contadores requer dois valores de exemplo para computar um valor que possa ser reproduzido.
ms.assetid: 75e45baf-51c5-400c-a31f-92bdab4ee492
title: Exibindo dados de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c56a2882485c0bf21db6f1f00788fb927442219f020b1241ab4cd64619c7ec56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794007"
---
# <a name="displaying-performance-data"></a>Exibindo dados de desempenho

A maioria dos contadores requer dois valores de exemplo para computar um valor que possa ser reproduzido. A fórmula para cada contador determina se o contador requer dois exemplos. para obter uma lista de contadores e suas fórmulas, consulte a seção tipos de contadores do [Kit de implantação do Windows Server 2003](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).

[Coletar dados de desempenho](collecting-performance-data.md) mostra como recuperar dados de exemplo. Depois de obter os exemplos, você normalmente chama [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue) para calcular um valor que pode ser displayável.

Se você precisar dimensionar o valor do contador para cima ou para baixo a fim de exibir o valor, chame a função [**PdhSetCounterScaleFactor**](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor) antes de chamar [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue). Os valores do contador podem ser dimensionados por uma potência de dez de um fator de-7 a 7.

Se o caminho do contador contiver um caractere curinga para o nome da instância, chame [**PdhGetFormattedCounterArray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya) para recuperar uma matriz de valores de contador formatados para cada instância coletada.

Você também pode usar as funções [**PdhCalculateCounterFromRawValue**](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue) e [**PdhFormatFromRawValue**](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue) para calcular um valor de exibição. Para usar essas funções, você deve recuperar o exemplo coletado após cada chamada de [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) e armazenar o exemplo por conta própria. Para recuperar o exemplo, chame a função [**PdhGetRawCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue) ou [**PdhGetRawCounterArray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya) . Para valores de contador baseados em tempo, chame [**PdhGetCounterTimeBase**](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase) antes de **PdhFormatFromRawValue** para recuperar a base de tempo do contador.

Se você executar cálculos usando os dados brutos, sempre verifique o membro **CStatus** da estrutura de [**\_ \_ contador bruto do PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) antes de usar o exemplo. O exemplo não será válido se o valor de **CStatus** não for PDH \_ CStatus \_ novos \_ dados ou PDH \_ CStatus \_ \_ dados válidos.

## <a name="displaying-statistics-for-a-counter"></a>Exibindo estatísticas para um contador

Se você quiser calcular os valores mínimo, máximo e médio de um contador, chame a função [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) . Ao coletar exemplos, armazene as estruturas de [**\_ \_ contador brutos de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) em uma matriz que você passa para **PdhComputeCounterStatistics**. A função retorna os valores estatísticos em uma estrutura de [**\_ estatísticas PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics) .

Você também pode usar essa função para compactar um arquivo de log. Por exemplo, leia dez registros de um arquivo de log, chame [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) para calcular o valor médio e, em seguida, grave o valor médio em um arquivo de log de saída.

 

 
