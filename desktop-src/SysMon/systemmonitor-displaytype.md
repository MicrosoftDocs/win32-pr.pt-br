---
title: Propriedade SystemMonitor. DisplayType
description: Recupera ou define o tipo de grafo usado para grafar os dados do contador de desempenho.
ms.assetid: a04545b1-920e-4fb3-909b-dc47e1374629
keywords:
- Propriedade de TipoDeExibição SysMon
- Propriedade doplaytype SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Propriedade TipoDeExibição
topic_type:
- apiref
api_name:
- SystemMonitor.DisplayType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c0e96ff0da57ef9e5f580063dc4f693d672e15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085607"
---
# <a name="systemmonitordisplaytype-property"></a>Propriedade SystemMonitor. DisplayType

Recupera ou define o tipo de grafo usado para grafar os dados do contador de desempenho.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Property DisplayType As DisplayTypeConstants
```



## <a name="property-value"></a>Valor da propriedade

Tipo de grafo usado para grafar os dados do contador de desempenho. Para obter os valores possíveis, consulte [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).

## <a name="exceptions"></a>Exceções



| Tipo de exceção               | Condição                                         |
|------------------------------|---------------------------------------------------|
| **System. ArgumentException** | O gráfico especificado ou o valor do relatório não é válido. |



 

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

 

 





