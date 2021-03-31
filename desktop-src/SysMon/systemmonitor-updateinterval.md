---
title: Propriedade SystemMonitor. UpdateInterval
description: Recupera ou define o período de tempo que o SYSMON espera antes da próxima vez que coleta dados do contador e atualiza o grafo ou relatório.
ms.assetid: 297931e4-23ae-4384-a04a-9c1fa8aa1239
keywords:
- Propriedade UpdateInterval SysMon
- Propriedade UpdateInterval SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Propriedade UpdateInterval
topic_type:
- apiref
api_name:
- SystemMonitor.UpdateInterval
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5872f870e831896ff37157a4a0f47584e77d93c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918372"
---
# <a name="systemmonitorupdateinterval-property"></a>Propriedade SystemMonitor. UpdateInterval

Recupera ou define o período de tempo que o SYSMON espera antes da próxima vez que coleta dados do contador e atualiza o grafo ou relatório.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Property UpdateInterval As Single
```



## <a name="property-value"></a>Valor da propriedade

Período de tempo, em segundos, que o SYSMON espera antes da próxima vez que coleta dados do contador e atualiza o grafo ou relatório. O intervalo mínimo é de 1 segundo (esse também é o valor padrão). O valor máximo é 1 milhão.

## <a name="remarks"></a>Comentários

Essa propriedade é relevante somente quando [**SystemMonitor. ManualUpdate**](systemmonitor-manualupdate.md) é definido como false.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





