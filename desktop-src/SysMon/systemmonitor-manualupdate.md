---
title: Propriedade SystemMonitor. ManualUpdate
description: Recupera ou define um valor que indica se o conteúdo do monitor do sistema será atualizado manualmente ou automaticamente em intervalos especificados.
ms.assetid: e068a955-ec1d-4f93-9261-25ba87773913
keywords:
- Propriedade ManualUpdate SysMon
- Propriedade ManualUpdate SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Propriedade ManualUpdate
topic_type:
- apiref
api_name:
- SystemMonitor.ManualUpdate
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1ecb426b47ba9cb7ec50b737f4f32d5ce274eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755772"
---
# <a name="systemmonitormanualupdate-property"></a>Propriedade SystemMonitor. ManualUpdate

Recupera ou define um valor que indica se o conteúdo do monitor do sistema será atualizado manualmente ou automaticamente em intervalos especificados.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Property ManualUpdate As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Verdadeiro indica que o grafo é atualizado manualmente. False indica que o grafo é atualizado automaticamente com base no intervalo de atualização especificado em [**SystemMonitor. UpdateInterval**](systemmonitor-updateinterval.md).

## <a name="remarks"></a>Comentários

Por padrão, o grafo é atualizado automaticamente.

Para atualizar o grafo manualmente, chame o método [**SystemMonitor. CollectSample**](systemmonitor-collectsample.md) .

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

[**SystemMonitor.CollectSample**](systemmonitor-collectsample.md)
</dt> <dt>

[**SystemMonitor.UpdateGraph**](systemmonitor-updategraph.md)
</dt> </dl>

 

 





