---
title: Propriedade SystemMonitor. ChartScroll
description: Recupera ou define um valor que determina se o gráfico de linha rola na exibição.
ms.assetid: df4806be-dfd3-4ff7-985d-b46c00bb19f8
keywords:
- Propriedade ChartScroll SysMon
- Propriedade ChartScroll SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, Propriedade ChartScroll
topic_type:
- apiref
api_name:
- SystemMonitor.ChartScroll
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51288af710e5ae94baf46acf0d2ed91732a1d310
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918551"
---
# <a name="systemmonitorchartscroll-property"></a>Propriedade SystemMonitor. ChartScroll

Recupera ou define um valor que determina se o gráfico de linha rola na exibição.

## <a name="syntax"></a>Syntax


```VB
Property ChartScroll As Boolean
```



## <a name="property-value"></a>Valor da propriedade

True se o grafo de linha rolar continuamente da direita para a esquerda; caso contrário, false se o grafo de linha for desenhado da esquerda para a direita e encapsulado sozinho na exibição. O padrão é false.

## <a name="remarks"></a>Comentários

Esse valor será ignorado se [**SystemMonitor. DisplayType**](systemmonitor-displaytype.md) não for [**DisplayTypeConstants.sysmonLineGraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





