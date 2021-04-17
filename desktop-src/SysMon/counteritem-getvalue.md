---
title: Método MyItem. GetValue
description: Recupera o último valor do contador.
ms.assetid: cf50d878-a119-42b0-bc59-b0e37ed15321
keywords:
- Método @ value SysMon
- Método GetValue SysMon, classe monoitem
- Classe monoitem SysMon, método GetValue
topic_type:
- apiref
api_name:
- CounterItem.GetValue
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e40950ce4a8bf24a6a4301db133779b34ce4ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749430"
---
# <a name="counteritemgetvalue-method"></a>Método MyItem. GetValue

Recupera o último valor do contador.

## <a name="syntax"></a>Sintaxe


```VB
CounterItem.GetValue( _
  ByRef value As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Último valor de amostra do contador.

</dd> <dt>

*status* \[ do fora\]
</dt> <dd>

Indica se o valor é válido.



| Valor                                                                                              | Significado                            |
|----------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>0</dt> </dl>                       | O valor é válido.<br/>     |
| <dl> <dt>0xC0000BBA (3221228474)</dt> </dl> | O valor não é válido.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se a origem dos dados do contador for de um arquivo de log, o valor será o último valor do contador no arquivo de log.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Item**](counteritem.md)
</dt> <dt>

[**MYITEM. getstatistics**](counteritem-getstatistics.md)
</dt> <dt>

[**MYITEM. Value**](counteritem-value.md)
</dt> </dl>

 

 





