---
description: A propriedade SWbemRefreshableItem.IsSet é um valor booliana que indica se o objeto SWbemRefreshableItem representa um único objeto ou um conjunto de objetos. O objeto SWbemRefreshableItem representa um único objeto ou um conjunto de objetos.
ms.assetid: 4be5d27c-9020-4150-84ce-f9efc55be947
ms.tgt_platform: multiple
title: Propriedade SWbemRefreshableItem.IsSet (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.get_IsSet
- ISWbemRefreshableItem.put_IsSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 055c776c1beffe1550033d61b54256d7b2e983ca70ac13f1b9fc899920910d4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312915"
---
# <a name="swbemrefreshableitemisset-property"></a>Propriedade SWbemRefreshableItem.IsSet

A **propriedade SWbemRefreshableItem.IsSet** é um valor booliana que indica se o objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) representa um único objeto ou um conjunto de objetos.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
SWbemRefreshableItem.IsSet As Boolean
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Se **SWbemRefreshableItem.IsSet** for **TRUE,** o item representará um objeto [**SWbemObjectSet**](swbemobjectset.md) e a propriedade [**Object**](swbemrefreshableitem-object.md) será **NULL.** Se **FALSE**, o item representará [**um objeto SWbemObject**](swbemobject.md) e **a propriedade Object** será **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefreshableItem<br/>                                                  |
| IID<br/>                      | IID \_ ISWbemRefreshableItem<br/>                                                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemRefreshableItem**](swbemrefreshableitem.md)
</dt> <dt>

[**SWbemRefreshableItem**](swbemrefresher.md)
</dt> </dl>

 

 




