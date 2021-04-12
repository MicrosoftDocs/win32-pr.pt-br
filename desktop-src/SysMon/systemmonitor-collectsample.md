---
title: Método SystemMonitor CollectSample
description: Obtém um valor para cada contador no objeto Counters.
ms.assetid: 4c91c759-597f-4aa8-aa77-eb181616e8b0
keywords:
- Método CollectSample SysMon
- Método CollectSample SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, método CollectSample
topic_type:
- apiref
api_name:
- SystemMonitor.CollectSample
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1c269d044c17a2ec1322fa969e0c86f468a901
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455273"
---
# <a name="systemmonitorcollectsample-method"></a>Método SystemMonitor:: CollectSample

Obtém um valor para cada contador no objeto [**Counters**](counters.md) .

## <a name="syntax"></a>Sintaxe


```VB
Sub CollectSample()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Chame **CollectSample** somente se [**ManualUpdate**](systemmonitor-manualupdate.md) for true e você estiver obtendo valores de contador de amostragem da atividade atual do computador não use esse método durante a amostragem de um arquivo de log. O grafo ou relatório é atualizado com o novo valor. Observe que alguns tipos de grafos precisam de dois exemplos para grafar os dados, por exemplo, o grafo de linha.

Para receber uma notificação quando o exemplo tiver sido coletado, implemente o evento [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Contadores**](counters.md)
</dt> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





