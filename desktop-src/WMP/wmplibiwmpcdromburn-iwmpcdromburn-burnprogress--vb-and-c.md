---
title: Propriedade IWMPCdrom Ltda burnProgress
description: A propriedade burnProgress obtém o progresso da gravação de CD conforme o percentual é concluído.
ms.assetid: 831cc55d-bd26-4328-a715-1a1fa48d7a40
keywords:
- propriedade burnProgress Windows Media Player
- propriedade burnProgress Windows Media Player , interface IWMPCdromEar
- Interface IWMPCdrom Ltda Windows Media Player , propriedade burnProgress
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnProgress
- IWMPCdromBurn.get_burnProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b8e468bc57bb40d990c0b2aeaffc23e184ef2ffa04ab85c9f60cf0d6bced57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332059"
---
# <a name="iwmpcdromburnburnprogress-property"></a>Propriedade IWMPCdrom Ltd::burnProgress

A **propriedade burnProgress** obtém o progresso da gravação de CD conforme o percentual é concluído.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Int32 burnProgress {get;}
```


```VB

Public ReadOnly Property burnProgress As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System.Int32 que** é o valor de progresso. Os valores de progresso variam de 0 a 100.

## <a name="remarks"></a>Comentários

O valor de progresso representa o percentual concluído de todo o processo de gravação, incluindo todas as operações de preparação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11<br/>                                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPCdrom Ltda (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





