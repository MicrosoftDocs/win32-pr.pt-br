---
title: Método SystemMonitor. GetLogViewRange
description: Recupera a data de início usada para recuperar valores de contadores dos arquivos de log.
ms.assetid: c74c3a5b-d2ec-43d8-b715-e399f42e8ae5
keywords:
- Método GetLogViewRange SysMon
- Método GetLogViewRange SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método GetLogViewRange
topic_type:
- apiref
api_name:
- SystemMonitor.GetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3233dd57327734669631fc57b31bfb85578621991f34c1b1c414a69697b82048
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882422"
---
# <a name="systemmonitorgetlogviewrange-method"></a>Método SystemMonitor. GetLogViewRange

Recupera a data de início usada para recuperar valores de contadores dos arquivos de log.

## <a name="syntax"></a>Sintaxe


```VB
SystemMonitor.GetLogViewRange( _
  ByRef StartTime As Date, _
  ByRef StopTime As Date _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartTime* \[ fora\]
</dt> <dd>

Data de início usada para recuperar valores de contadores dos arquivos de log.

</dd> <dt>

*StopTime* \[ fora\]
</dt> <dd>

Data de término usada para recuperar valores de contadores dos arquivos de log.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O SYSMON recupera valores de contadores dos arquivos de log que se enquadram nas datas de início e parada, inclusive.

Usar esse método é o mesmo que acessar as propriedades [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) e [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





