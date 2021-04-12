---
title: Propriedade Counters. Item
description: Recupera a instância de monoitem especificada da coleção.
ms.assetid: bf503371-c8bd-4e0d-ab8d-58de3f8fac5f
keywords:
- Propriedade do item SysMon
- Propriedade de item SysMon, classe de contadores
- Classe Counters SysMon, Propriedade Item
topic_type:
- apiref
api_name:
- Counters.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251a645f0a4ceacdbfb4e2ab7e650f41e44dd508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454849"
---
# <a name="countersitem-property"></a>Propriedade Counters. Item

Recupera a instância de [**monoitem**](counteritem.md) especificada da coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Property Item( _
  ByVal index As Object _
) As CounterItem
```



## <a name="property-value"></a>Valor da propriedade

Instância de [**monoitem**](counteritem.md) que corresponde ao valor de índice especificado.

## <a name="exceptions"></a>Exceções



| Tipo de exceção                                  | Condição                         |
|-------------------------------------------------|-----------------------------------|
| **System. Runtime. InteropServices. COMException** | O índice especificado não é válido. |



 

## <a name="remarks"></a>Comentários

Essa é a propriedade padrão do objeto [**Counters**](counters.md) .

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

[**Contadores**](counters.md)
</dt> </dl>

 

 





