---
description: A propriedade SWbemRefreshableItem. IsSet é um valor booliano que indica se o objeto SWbemRefreshableItem representa um único objeto ou um conjunto de objetos. O objeto SWbemRefreshableItem representa um único objeto ou um conjunto de objetos.
ms.assetid: 4be5d27c-9020-4150-84ce-f9efc55be947
ms.tgt_platform: multiple
title: Propriedade SWbemRefreshableItem. IsSet (Wbemdisp. h)
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
ms.openlocfilehash: 71fb5f84ec7ad35f1d9beab32cb74db5b7591057
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105790537"
---
# <a name="swbemrefreshableitemisset-property"></a>Propriedade SWbemRefreshableItem. IsSet

A propriedade **SWbemRefreshableItem. IsSet** é um valor booliano que indica se o objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) representa um único objeto ou um conjunto de objetos.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
SWbemRefreshableItem.IsSet As Boolean
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Se **SWbemRefreshableItem. IsSet** for **true**, o item representará um objeto [**SWbemObjectSet**](swbemobjectset.md) e a propriedade [**Object**](swbemrefreshableitem-object.md) será **NULL**. Se **for false**, o item representará um objeto [**SWbemObject**](swbemobject.md) e a propriedade **Object** será **nula**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMREFRESHABLEITEM CLSID<br/>                                                  |
| IID<br/>                      | ISWbemRefreshableItem de IID \_<br/>                                                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemRefreshableItem**](swbemrefreshableitem.md)
</dt> <dt>

[**SWbemRefreshableItem**](swbemrefresher.md)
</dt> </dl>

 

 




