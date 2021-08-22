---
title: Propriedade errorContext de IWMPErrorItem
description: A propriedade errorContext obtém um valor que indica o contexto do erro.
ms.assetid: e9ebd636-e611-49c6-9533-a02ff74db7bc
keywords:
- Propriedade errorContext Windows Media Player
- propriedade errorContext Windows Media Player interface , IWMPErrorItem
- Interface IWMPErrorItem Windows Media Player , propriedade errorContext
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorContext
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60320df74d139e1cba3802c664ebff96e4531f569cd3321ae8821fc89ea5b0fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053644"
---
# <a name="iwmperroritemerrorcontext-property"></a>Propriedade IWMPErrorItem::errorContext

A **propriedade errorContext** obtém um valor que indica o contexto do erro.

## <a name="syntax"></a>Syntax


```CSharp
public System.Object errorContext {get; set;}
```


```VB

Public ReadOnly Property errorContext As System.Object
```





## <a name="property-value"></a>Valor da propriedade

Um **System.Object que** é o contexto de erro.

## <a name="remarks"></a>Comentários

O contexto de erro são informações que são usadas pela Microsoft para fornecer informações adicionais para a equipe de suporte técnico.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPErrorItem (VB e C#)**](iwmperroritem--vb-and-c.md)
</dt> </dl>

 

 





