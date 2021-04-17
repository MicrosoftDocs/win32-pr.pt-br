---
title: SystemMonitor.Batmétodo chingLock
description: Bloqueia o monitor do sistema para impedi-lo de amostragem de dados do contador do contador ou arquivo de log recém-adicionado.
ms.assetid: 6b9d683a-7a97-44a4-9eb6-6caaafe2abdd
keywords:
- Método BatchingLock SysMon
- Método BatchingLock SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método BatchingLock
topic_type:
- apiref
api_name:
- SystemMonitor.BatchingLock
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b858a6920b039d911ae571d81744eb99dea4ef4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762878"
---
# <a name="systemmonitorbatchinglock-method"></a>SystemMonitor.Batmétodo chingLock

Bloqueia o monitor do sistema para impedi-lo de amostragem de dados do contador do contador ou arquivo de log recém-adicionado.

## <a name="syntax"></a>Sintaxe


```VB
SystemMonitor.BatchingLock( _
  ByVal lock As Boolean, _
  ByVal batchReason As SysmonBatchReason _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Bloquear* \[ no\]
</dt> <dd>

Defina como true para bloquear o monitor do sistema para impedir que ele faça amostragem de dados do contador do contador ou arquivo de log recém-adicionado. Defina como false para remover o bloqueio.

</dd> <dt>

*batchReason* \[ no\]
</dt> <dd>

Identifica a origem dos dados que você está bloqueando. Use o mesmo valor de motivo ao bloquear e desbloquear o recurso. Para obter os valores possíveis, consulte a enumeração [**SysmonBatchReason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Você deve chamar esse método duas vezes, uma vez para bloquear a origem (true) e uma vez para desbloquear a origem (false).

Você pode posicionar apenas um bloqueio. Por exemplo, se você definir o bloqueio para SysmonBatchAddFiles e, em seguida, fizer uma segunda chamada usando SysmonBatchAddCounters como o motivo, a segunda chamada removerá o bloqueio colocado pela primeira chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





