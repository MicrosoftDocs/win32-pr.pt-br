---
title: Propriedade SystemMonitor.DataPointCount
description: Recupera ou define o número de pontos de dados exibidos em um grafo de linha.
ms.assetid: bc1a86c2-635b-4e93-ac96-e7be4b1d375a
keywords:
- Propriedade DataPointCount SysMon
- Propriedade DataPointCount SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon , propriedade DataPointCount
topic_type:
- apiref
api_name:
- SystemMonitor.DataPointCount
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d7d1212f3f1467c0fb505e84dffdd9cc6bb381c19d8ccc34ad38ee46562ec6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882617"
---
# <a name="systemmonitordatapointcount-property"></a>Propriedade SystemMonitor.DataPointCount

Recupera ou define o número de pontos de dados exibidos em um grafo de linha.

## <a name="syntax"></a>Syntax


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a>Valor da propriedade

Número de pontos de dados exibidos na exibição de um grafo de linha. O valor padrão é 100 pontos de dados. O intervalo válido de valores é de 2 a 1.000.

## <a name="remarks"></a>Comentários

Essa propriedade será usada somente se [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) **for sysmonCurrentActivity**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





