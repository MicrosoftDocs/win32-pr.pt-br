---
description: o desempenho formatado do WMI de alto desempenho Provedor de Dados calcula os tipos de contadores estatísticos em um número especificado de amostras de dados de contador bruto.
ms.assetid: a7e32ef2-fad1-449c-beee-07db4b93e3fe
ms.tgt_platform: multiple
title: Tipos de contadores estatísticos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1289bae423305bac863afefaba8e5700268d98e594fe767d597c8470aa4f1ac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314815"
---
# <a name="statistical-counter-types"></a>Tipos de contadores estatísticos

o [desempenho formatado](formatted-performance-data-provider.md) do WMI de alto desempenho Provedor de Dados calcula os tipos de contadores estatísticos em um número especificado de amostras de dados de contador bruto. Os algoritmos para os tipos de contador não exigem Propriedades de frequência ou carimbo de data/hora herdadas (como **carimbo de data/hora \_** ou **frequência \_ PerfTime**) que outros tipos de contador exigem.

Em vez disso, os tipos de contadores estatísticos dão suporte a um **qualificador** que identifica quantas amostras usar. Um exemplo é coletado quando o método [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) é chamado para o objeto de desempenho. Para scripts, use o método [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) . Os dados calculados contêm o resultado do cálculo realizado no número **SampleWindow** de amostras da propriedade dados brutos. Os dados brutos do cálculo vêm de frm o nome da propriedade especificada no qualificador do **contador** .

Para obter mais informações, consulte [obtendo dados de desempenho estatísticos](obtaining-statistical-performance-data.md) e [acessando classes de desempenho de WMI pré-instalado](accessing-wmi-preinstalled-performance-classes.md).



| Constante de tipo                    | Descrição                                                                                                                                                                                |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [média de COOKER \_](cooker-average.md)   | Soma observações repetidas de uma propriedade em uma classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e divide a soma pelo número de observações.                              |
| [COOKER \_ Max](cooker-max.md)           | Maior valor de um conjunto de observações de uma propriedade em uma classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .                                                                    |
| [COOKER \_ mín.](cooker-min.md)           | Menor valor de um conjunto de observações de uma propriedade em uma classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .                                                                   |
| [intervalo de COOKER \_](cooker-range.md)       | Diferença entre os valores [mínimo](cooker-min.md) e [máximo](cooker-max.md) para um conjunto de observações brutas de uma propriedade em uma classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) . |
| [variância de COOKER \_](cooker-variance.md) | Medida de variabilidade que pode ser usada para caracterizar a dispersão de um conjunto de observações brutas de uma propriedade em uma classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de contador de desempenho WMI](wmi-performance-counter-types.md)
</dt> <dt>

[Monitorando dados de desempenho](monitoring-performance-data.md)
</dt> <dt>

[Atualizando dados do WMI em scripts](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[Acessando dados de desempenho no script](accessing-performance-data-in-script.md)
</dt> <dt>

[Acessando dados de desempenho em C++](accessing-performance-data-in-c--.md)
</dt> </dl>

 

 
