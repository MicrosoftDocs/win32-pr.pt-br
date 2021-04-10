---
description: O tipo de contador de desempenho designa uma fórmula necessária para obter contadores de desempenho calculados. Esses são os mesmos tipos de contador usados pelo monitoramento de desempenho do Windows.
ms.assetid: d4a9feca-80a2-4ce5-b4d7-4e83ef951c08
ms.tgt_platform: multiple
title: Tipos de contador de desempenho WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ac0d2c8afb1499fec44c983364b5e3278b864
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091370"
---
# <a name="wmi-performance-counter-types"></a>Tipos de contador de desempenho WMI

O [tipo de contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) de desempenho designa uma fórmula necessária para obter contadores de desempenho calculados. Esses são os mesmos tipos de contador usados pelo [monitoramento de desempenho](/windows/desktop/PerfCtrs/performance-counters-portal)do Windows. Nas classes de desempenho WMI, os dados brutos para a fórmula de tipo de contador vêm de uma classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e o resultado calculado é encontrado na propriedade de mesmo nome de uma classe [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) correspondente.

Os tipos de contadores aparecem como o qualificador de **tipo** de propriedade nas classes [**\_ PerfRawData do Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e como o qualificador de **Culináriatype** para propriedades em classes [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .

Por exemplo, a propriedade **AvgDiskBytesPerRead** na classe [**\_ PerfRawData do \_ backfdisk \_ do Win32**](./retrieving-raw-and-formatted-performance-data.md) é a fonte de dados brutos para a propriedade **AvgDiskBytesPerRead** na classe [**Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), que contém os mesmos dados, conforme mostrado no monitor do sistema.

A lista a seguir organiza as descrições de tipo de contador por tipo funcional:

-   [Tipos de contador base](base-counter-types.md)
-   [Tipos de contador de algoritmos básicos](basic-algorithm-counter-types.md)
-   [Tipos de contadores de algoritmo de contador](counter-algorithm-counter-types.md)
-   [Tipos de contadores não computacionais](noncomputational-counter-types.md)
-   [Tipos de contadores de algoritmo de timer de precisão](precision-timer-algorithm-counter-types.md)
-   [Tipos de contadores de algoritmo de comprimento de fila](queue-length-algorithm-counter-types.md)
-   [Tipos de contadores estatísticos](statistical-counter-types.md)
-   [Tipos de contadores de algoritmo de temporizador](timer-algorithm-counter-types.md)

 

 
