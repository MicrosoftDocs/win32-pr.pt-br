---
title: O que há de novo no monitor do sistema
description: A tabela a seguir identifica o que há de novo para cada versão do monitor do sistema (SYSMON).
ms.assetid: 9cb0e0db-0933-4993-a995-74a36a24eccb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3662e83954630232e3fe30c26a3f6d94aa9cc7
ms.sourcegitcommit: 780d4b1601c45658ef0b799b80d13f45a53d808d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2020
ms.locfileid: "104365678"
---
# <a name="whats-new-in-system-monitor"></a>O que há de novo no monitor do sistema

A tabela a seguir identifica o que há de novo para cada versão do monitor do sistema (SYSMON).



| Versão     | Descrição dos recursos                                                                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão 3,7 | Essa versão adiciona novos tipos de grafo, a capacidade de selecionar vários contadores, recuperar valores de contador de um ponto no grafo, salvar valores de contador grafado em um arquivo de log e a opção de ter um grafo de linha rolando continuamente na janela do grafo em vez de encapsular sozinho. Incluído no Windows Server 2008 e no Windows Vista.<br/> |



 

## <a name="version-37"></a>Versão 3,7

Novas propriedades e métodos que foram adicionados ao [**MYITEM**](counteritem.md).

-   [**GetDataAt**](counteritem-getdataat.md)
-   [**Selected**](counteritem-selected.md)
-   [**Visible**](counteritem-visible.md)
-   Intervalo de valores válidos alterado para [ **MyItem. Width**](counteritem-width.md)

Novas propriedades e métodos que foram adicionados a [**SystemMonitor**](systemmonitor.md).

-   [**BatchingLock**](systemmonitor-batchinglock.md)
-   [**ChartScroll**](systemmonitor-chartscroll.md)
-   [**ClearData**](systemmonitor-cleardata.md)
-   [**DataPointCount**](systemmonitor-datapointcount.md)
-   [**EnableDigitGrouping**](systemmonitor-enabledigitgrouping.md)
-   [**EnableToolTips**](systemmonitor-enabletooltips.md)
-   [**GetLogViewRange**](systemmonitor-getlogviewrange.md)
-   [**LoadSettings**](systemmonitor-loadsettings.md)
-   [**LogSourceStartTime**](systemmonitor-logsourcestarttime.md)
-   [**LogSourceStopTime**](systemmonitor-logsourcestoptime.md)
-   [**Relog**](systemmonitor-relog.md)
-   [**SaveAs**](systemmonitor-saveas.md)
-   [**ScaleToFit**](systemmonitor-scaletofit.md)
-   [**SetLogViewRange**](systemmonitor-setlogviewrange.md)
-   [**ShowTimeAxisLables**](systemmonitor-showtimeaxislabels.md)

Novas enumerações que foram adicionadas.

-   [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype)
-   [**SysmonFileType**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype)
-   Novos valores de tipo de exibição foram adicionados a [ **DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)

 

 





