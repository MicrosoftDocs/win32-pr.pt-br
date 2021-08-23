---
title: Propriedade SystemMonitor SqlLogSetName
description: Recupera ou define o nome amigável do conjunto de log.
ms.assetid: a4593743-6b70-4f70-8e91-3324a808d97b
keywords:
- Propriedade SqlLogSetName SysMon
- Propriedade SqlLogSetName SysMon, interface SystemMonitor
- Interface systemMonitor SysMon, propriedade SqlLogSetName
topic_type:
- apiref
api_name:
- SystemMonitor.SqlLogSetName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce06e396b6a90a46de88d915a0191258da723bef31dfe82f67a20c9507b2939d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118881303"
---
# <a name="systemmonitorsqllogsetname-property"></a>Propriedade SystemMonitor::SqlLogSetName

Recupera ou define o nome amigável do conjunto de log.

## <a name="syntax"></a>Syntax


```VB
Property SqlLogSetName As String
```



## <a name="property-value"></a>Valor da propriedade

Nome amigável do conjunto de log, que corresponde a um único arquivo de log que contém dados binários ou de texto no banco de dados SQL dados.

## <a name="remarks"></a>Comentários

**Antes do Windows Vista:** Você não poderá modificar essa propriedade se o valor [**de SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) for definido como sysmonSqlLog.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.SqlDsnName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





