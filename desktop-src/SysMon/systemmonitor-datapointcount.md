---
title: Propriedade SystemMonitor. DataPointCount
description: Recupera ou define o número de pontos de dados exibidos em um grafo de linha.
ms.assetid: bc1a86c2-635b-4e93-ac96-e7be4b1d375a
keywords:
- Propriedade DataPointCount SysMon
- Propriedade DataPointCount SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, Propriedade DataPointCount
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
ms.openlocfilehash: fffb8b39216895ce4ebce6924ca7cc99b5366cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918220"
---
# <a name="systemmonitordatapointcount-property"></a>Propriedade SystemMonitor. DataPointCount

Recupera ou define o número de pontos de dados exibidos em um grafo de linha.

## <a name="syntax"></a>Syntax


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a>Valor da propriedade

Número de pontos de dados exibidos na exibição de um gráfico de linhas. O valor padrão é 100 pontos de dados. O intervalo válido de valores é de 2 a 1.000.

## <a name="remarks"></a>Comentários

Essa propriedade será usada somente se [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) for **sysmonCurrentActivity**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





