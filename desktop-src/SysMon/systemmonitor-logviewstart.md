---
title: Propriedade SystemMonitor. LogViewStart
description: Recupera ou define a data de início usada para recuperar valores de contadores dos arquivos de log.
ms.assetid: f9fdef17-e8b1-4efb-86db-40ca0c499194
keywords:
- Propriedade LogViewStart SysMon
- Propriedade LogViewStart SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Propriedade LogViewStart
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStart
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc1c7c4a46ac746582d62ee7ce08980b078eb8d972cb6b4d3ed787b49f2285f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117955399"
---
# <a name="systemmonitorlogviewstart-property"></a>Propriedade SystemMonitor. LogViewStart

Recupera ou define a data de início usada para recuperar valores de contadores dos arquivos de log.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Property LogViewStart As Date
```



## <a name="property-value"></a>Valor da propriedade

Data de início usada para recuperar valores de contadores dos arquivos de log.

## <a name="remarks"></a>Comentários

O SYSMON recupera valores de contadores dos arquivos de log que se enquadram nas datas inicial e [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) , inclusive.

Se você não especificar uma data de início ou se definir essa propriedade como um valor de data que está fora do intervalo de valores de data encontrado nos arquivos de log, o SYSMON alterará o valor para o valor de data mais anterior encontrado nos arquivos de log.

Se essa propriedade for definida como um valor de data maior que [**LogViewStop**](systemmonitor-logviewstop.md), o SYSMON alterará o valor para o valor de **LogViewStop**.

Se você especificar uma data de início e de parada, deverá especificar as datas antes de definir [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.GetLogViewRange**](systemmonitor-getlogviewrange.md)
</dt> <dt>

[**SystemMonitor. LogFiles**](systemmonitor-logfiles.md)
</dt> <dt>

[**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md)
</dt> <dt>

[**SystemMonitor.LogSourceStartTime**](systemmonitor-logsourcestarttime.md)
</dt> <dt>

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





