---
title: Método MyItem. GetDataAt
description: Recupera o valor do contador especificado de um ponto específico no grafo.
ms.assetid: e8484301-4575-41ee-9c6d-a454eca0e82d
keywords:
- Método GetDataAt SysMon
- Método GetDataAt SysMon, objeto monoitem
- Objeto monoitem SysMon, método GetDataAt
topic_type:
- apiref
api_name:
- CounterItem.GetDataAt
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354d8242e6cb765980878a7783805416bb1a1009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499422"
---
# <a name="counteritemgetdataat-method"></a>Método MyItem. GetDataAt

Recupera o valor do contador especificado de um ponto específico no grafo.

## <a name="syntax"></a>Sintaxe


```VB
CounterItem.GetDataAt( _
  ByVal index As Long, _
  ByVal which As SysmonDataType, _
  ByRef variant As Object _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

Índice de base zero do ponto do grafo cujo valor você deseja recuperar. Os valores válidos variam de 0 a ([**SystemMonitor. DataPointCount**](systemmonitor-datapointcount.md) -1).

</dd> <dt>

*que* \[ no\]
</dt> <dd>

Tipo de valor do contador a recuperar, por exemplo, o valor médio do contador, conforme exibido na janela do grafo. Para obter os valores possíveis, consulte [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).

</dd> <dt>

*variante* \[ fora\]
</dt> <dd>

Valor do contador que foi recuperado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Use este método somente se

-   [**SystemMonitor. DisplayType**](systemmonitor-displaytype.md) está definido como sysmonLineGraph
-   [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) é definido como SysmonLogFiles ou sysmonSqlLog

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Item**](counteritem.md)
</dt> <dt>

[**MYITEM. getstatistics**](counteritem-getstatistics.md)
</dt> <dt>

[**MYITEM. GetValue**](counteritem-getvalue.md)
</dt> </dl>

 

 





