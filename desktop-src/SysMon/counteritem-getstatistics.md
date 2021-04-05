---
title: Método MyItem. getstatistics
description: Recupera os valores médio, máximo e mínimo para o contador.
ms.assetid: fb55d68b-1dbe-48b1-88c8-51f33048ec24
keywords:
- Método getstatistics SysMon
- Método getstatistics SysMon, classe de coitem
- Classe monoitem SysMon, método getstatistics
topic_type:
- apiref
api_name:
- CounterItem.GetStatistics
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c993ed8b9bb39a4d8bb3ff18663f2d884ece156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918577"
---
# <a name="counteritemgetstatistics-method"></a>Método MyItem. getstatistics

Recupera os valores médio, máximo e mínimo para o contador.

## <a name="syntax"></a>Sintaxe


```VB
CounterItem.GetStatistics( _
  ByRef max As Double, _
  ByRef min As Double, _
  ByRef average As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*máximo* \[ fora\]
</dt> <dd>

Valor máximo do contador.

</dd> <dt>

*mín* \[ . fora\]
</dt> <dd>

Valor mínimo do contador.

</dd> <dt>

*média* \[ fora\]
</dt> <dd>

Valor médio do contador.

</dd> <dt>

*status* \[ do fora\]
</dt> <dd>

Indica se os valores são válidos.



| Valor                                                                                              | Significado                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>0</dt> </dl>                       | Os valores são válidos.<br/>     |
| <dl> <dt>0xC0000BBA (3221228474)</dt> </dl> | Os valores não são válidos.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Somente os valores de contador visíveis na janela do Graph são usados para calcular os valores estatísticos.

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

[**MYITEM. GetDataAt**](counteritem-getdataat.md)
</dt> <dt>

[**MYITEM. GetValue**](counteritem-getvalue.md)
</dt> </dl>

 

 





