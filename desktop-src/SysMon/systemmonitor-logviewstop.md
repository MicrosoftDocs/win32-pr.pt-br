---
title: Propriedade SystemMonitor.LogViewStop
description: Recupera ou define a data de término usada para recuperar valores de contador dos arquivos de log.
ms.assetid: 5dabfb26-fa33-4fb5-a075-ed8955a56f1e
keywords:
- Propriedade LogViewStop SysMon
- Propriedade LogViewStop SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, propriedade LogViewStop
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStop
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8c30305f99e0d9bf66dd0f00dccc7674073e0f7058bca4284411c9d24426b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882070"
---
# <a name="systemmonitorlogviewstop-property"></a>Propriedade SystemMonitor.LogViewStop

Recupera ou define a data de término usada para recuperar valores de contador dos arquivos de log.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Property LogViewStop As Date
```



## <a name="property-value"></a>Valor da propriedade

Data de término usada para recuperar valores de contador dos arquivos de log.

## <a name="remarks"></a>Comentários

O SYSMON recupera valores de contador dos arquivos de log que se enquadram no [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) e param as datas, inclusive.

Se você não especificar um valor de parada ou definir essa propriedade como um valor de data posterior à última data contida no arquivo de log, o SYSMON altera o valor para o valor de data mais recente encontrado nos arquivos de log.

Se essa propriedade for definida como um valor de data menor que [**LogViewStart,**](systemmonitor-logviewstart.md)o SYSMON altera o valor para o **valor de LogViewStart.**

Você deve definir a data de início antes de definir a data de parada; caso contrário, ambos os valores serão definidos como Date.MinValue e, se você definir as datas depois de definir [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md), somente o primeiro valor do contador será recuperado do arquivo de log.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.GetLogViewRange**](systemmonitor-getlogviewrange.md)
</dt> <dt>

[**SystemMonitor.LogSourceStopTime**](systemmonitor-logsourcestoptime.md)
</dt> <dt>

[**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md)
</dt> <dt>

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





