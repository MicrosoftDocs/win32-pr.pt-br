---
title: Propriedade SystemMonitor.EnableDigitGrouping
description: Recupera ou define um valor que determina se o SYSMON usa o grupo de dígitos ao exibir valores numéricos.
ms.assetid: 6a277960-fd01-423c-af2a-b35ed46c6d9a
keywords:
- Propriedade EnableDigitGrouping SysMon
- Propriedade EnableDigitGrouping SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon , propriedade EnableDigitGrouping
topic_type:
- apiref
api_name:
- SystemMonitor.EnableDigitGrouping
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d910e479cc0a957ea5f1332d7fead0f93badd797bfe2d90b26f9914f0c3d863a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882601"
---
# <a name="systemmonitorenabledigitgrouping-property"></a>Propriedade SystemMonitor.EnableDigitGrouping

Recupera ou define um valor que determina se o SYSMON usa o grupo de dígitos ao exibir valores numéricos.

## <a name="syntax"></a>Syntax


```VB
Property EnableDigitGrouping As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se True, o SYSMON agrupará dígitos ao exibir valores numéricos, por exemplo, 1.214. Se False, os valores numéricos não serão agrupados, por exemplo, 1214. True é o padrão.

## <a name="remarks"></a>Comentários

O símbolo de grupo de dígitos é localizado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





