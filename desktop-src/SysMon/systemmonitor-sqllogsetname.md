---
title: Propriedade SystemMonitor SqlLogSetName
description: Recupera ou define o nome amigável do conjunto de logs.
ms.assetid: a4593743-6b70-4f70-8e91-3324a808d97b
keywords:
- Propriedade SqlLogSetName SysMon
- Propriedade SqlLogSetName SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, Propriedade SqlLogSetName
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
ms.openlocfilehash: be20ccc561eb3e9292b4a95dcc654ed7bac00ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008823"
---
# <a name="systemmonitorsqllogsetname-property"></a>Propriedade SystemMonitor:: SqlLogSetName

Recupera ou define o nome amigável do conjunto de logs.

## <a name="syntax"></a>Syntax


```VB
Property SqlLogSetName As String
```



## <a name="property-value"></a>Valor da propriedade

Nome amigável do conjunto de logs, que corresponde a um único arquivo de log que contém dados binários ou de texto no SQL Database.

## <a name="remarks"></a>Comentários

**Antes do Windows Vista:** Você não poderá modificar essa propriedade se o valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) estiver definido como sysmonSqlLog.

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

[**SystemMonitor.SqlDsnName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





