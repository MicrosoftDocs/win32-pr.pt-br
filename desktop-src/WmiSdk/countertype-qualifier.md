---
description: O qualificador de tipo contém o valor inteiro para o tipo de contador de propriedade para propriedades em \_ classes PerfRawData do Win32. O Culináriatype contém as constantes para tipos de fórmulas de propriedade em \_ classes PerfFormattedData do Win32.
ms.assetid: aa79fcdb-503f-4928-b2b7-f07baeaf9fb5
ms.tgt_platform: multiple
title: Qualificador de tipo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 883ee7aa2f230756d62294d46e6402fe7f962d4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768617"
---
# <a name="countertype-qualifier"></a>Qualificador de tipo

O qualificador de **tipo** contém o valor inteiro para o tipo de contador de propriedade para propriedades em classes [**\_ PerfRawData do Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) . O **culináriatype** contém as constantes para tipos de fórmulas de propriedade em classes [**\_ PerfFormattedData do Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .

Para obter mais informações e uma divisão dos tipos de contadores por função, consulte [tipos de contadores](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).



| CounterType | Culináriatype                              |
|-------------|------------------------------------------|
| 0           | contador de desempenho \_ \_ RAWCOUNT \_ hex             |
| 256         | contador de desempenho \_ \_ grande \_ RAWCOUNT \_ hex      |
| 2816        | \_texto do contador de desempenho \_                      |
| 65536       | contador de desempenho \_ \_ RAWCOUNT                  |
| 65792       | contador de desempenho \_ \_ grande \_ RAWCOUNT           |
| 73728       | PERF \_ duplo \_ bruto                        |
| 4195328     | \_Delta do contador de desempenho \_                     |
| 4195584     | \_ \_ Delta grande do contador de desempenho \_              |
| 4260864     | \_contador de exemplo de desempenho \_                    |
| 4523008     | \_tipo de \_ QUEUELEN do contador de desempenho \_            |
| 4523264     | \_tipo de \_ \_ QUEUELEN grande do contador \_ de desempenho     |
| 5571840     | Tipo de QUEUELEN do contador de desempenho de \_ \_ 100 NS \_ \_     |
| 6620416     | \_tipo de \_ QUEUELEN de tempo de obj do contador de \_ \_ desempenho \_ |
| 272696320   | \_contador de contador de desempenho \_                   |
| 272696576   | \_ \_ contagem em massa do contador de desempenho \_               |
| 537003008   | \_fração bruta de desempenho \_                      |
| 541132032   | \_Timer do contador de desempenho \_                     |
| 541525248   | \_ \_ temporizador do sistema de precisão de desempenho \_           |
| 542180608   | \_ \_ Temporizador 100NSEC perf                     |
| 542573824   | \_ \_ Temporizador de 100ns de precisão de desempenho \_            |
| 543229184   | \_ \_ temporizador de tempo de obj perf \_                   |
| 543622400   | \_ \_ temporizador de objeto de precisão de desempenho \_           |
| 549585920   | \_fração de exemplo de perf \_                   |
| 557909248   | Timer do contador de desempenho \_ \_ \_ inv                |
| 558957824   | \_Contador de \_ temporizador 100NSEC de desempenho \_ inv                |
| 574686464   | \_ \_ múltiplo Timer do contador de desempenho \_              |
| 575735040   | \_Timer de \_ vários \_ 100NSEC perf              |
| 591463680   | \_ \_ multi timer de \_ contador de desempenho \_         |
| 592512256   | PERF \_ 100NSEC \_ multi \_ timer \_ inv         |
| 805438464   | \_temporizador de média de desempenho \_                     |
| 807666944   | \_tempo decorrido de desempenho \_                      |
| 1073742336  | contador de desempenho \_ \_ NODATA                    |
| 1073874176  | \_massa média de desempenho \_                      |
| 1073939457  | \_base de exemplo de perf \_                       |
| 1073939458  | \_base média de desempenho \_                      |
| 1073939459  | \_base bruta de desempenho \_                          |
| 1073939712  | \_timestamp de precisão de desempenho \_               |
| 1073939715  | \_ \_ base bruta de perf grande \_                   |
| 1107494144  | \_ \_ vários base do contador de desempenho \_               |
| 2147483648  | \_tipo de \_ histograma do contador de desempenho \_           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Qualificadores específicos para classes de desempenho WMI](qualifiers-specific-to-wmi-performance-classes.md)
</dt> </dl>

 

