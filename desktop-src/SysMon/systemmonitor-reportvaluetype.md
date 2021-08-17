---
title: Propriedade SystemMonitor. ReportValueType
description: Recupera ou define um valor que determina se as exibições de histograma e relatório exibem o último valor amostrado durante o intervalo de amostragem ou um valor calculado da amostragem, como o valor médio ou mínimo do contador.
ms.assetid: add75744-c3ab-48ab-b567-28a072facfdd
keywords:
- Propriedade ReportValueType SysMon
- Propriedade ReportValueType SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Propriedade ReportValueType
topic_type:
- apiref
api_name:
- SystemMonitor.ReportValueType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95282c48ac30b13af07c124ea21f36f91c7ae658b10d290a109fdd1dcc7a5ee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117955004"
---
# <a name="systemmonitorreportvaluetype-property"></a>Propriedade SystemMonitor. ReportValueType

Recupera ou define um valor que determina se as exibições de histograma e relatório exibem o último valor amostrado durante o intervalo de amostragem ou um valor calculado da amostragem, como o valor médio ou mínimo do contador.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Property ReportValueType As ReportValueTypeConstants
```



## <a name="property-value"></a>Valor da propriedade

Determina se o histograma e os modos de exibição de relatório exibem o último valor amostrado durante o intervalo de amostragem ou um valor calculado a partir do intervalo de amostragem. Para obter os valores possíveis, consulte [**ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).

## <a name="remarks"></a>Comentários

O SYSMON ignora esse valor e usa [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) se [**SystemMonitor. DisplayType**](systemmonitor-displaytype.md) não for [**DisplayTypeConstants.sysmonHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) ou **DisplayTypeConstants.sysmonReport**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





