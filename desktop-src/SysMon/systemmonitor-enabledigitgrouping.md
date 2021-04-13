---
title: Propriedade SystemMonitor. EnableDigitGrouping
description: Recupera ou define um valor que determina se o SYSMON usa o agrupamento de dígitos ao exibir valores numéricos.
ms.assetid: 6a277960-fd01-423c-af2a-b35ed46c6d9a
keywords:
- Propriedade EnableDigitGrouping SysMon
- Propriedade EnableDigitGrouping SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, Propriedade EnableDigitGrouping
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
ms.openlocfilehash: 66da0ad5ade7f3e01f58ef29bbd1094634c01b37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369645"
---
# <a name="systemmonitorenabledigitgrouping-property"></a>Propriedade SystemMonitor. EnableDigitGrouping

Recupera ou define um valor que determina se o SYSMON usa o agrupamento de dígitos ao exibir valores numéricos.

## <a name="syntax"></a>Syntax


```VB
Property EnableDigitGrouping As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se for true, o SYSMON agrupará dígitos ao exibir valores numéricos, por exemplo, 1.214. Se for false, os valores numéricos não serão agrupados, por exemplo, 1214. True é o padrão.

## <a name="remarks"></a>Comentários

O símbolo de agrupamento de dígitos está localizado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





