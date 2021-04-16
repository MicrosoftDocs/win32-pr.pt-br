---
title: Propriedade IWMPCdromBurn burnProgress
description: A propriedade burnProgress Obtém o progresso da gravação do CD como porcentagem concluída.
ms.assetid: 831cc55d-bd26-4328-a715-1a1fa48d7a40
keywords:
- Propriedade burnProgress Windows Media Player
- Propriedade burnProgress Windows Media Player, interface IWMPCdromBurn
- Interface IWMPCdromBurn Windows Media Player, Propriedade burnProgress
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
ms.openlocfilehash: 835c8c1091941437c226427ddb3ef53e8c577b5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761634"
---
# <a name="iwmpcdromburnburnprogress-property"></a>Propriedade IWMPCdromBurn:: burnProgress

A propriedade **burnProgress** Obtém o progresso da gravação do CD como porcentagem concluída.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Int32 burnProgress {get;}
```


```VB

Public ReadOnly Property burnProgress As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é o valor de progresso. Os valores de progresso variam de 0 a 100.

## <a name="remarks"></a>Comentários

O valor de progresso representa a porcentagem completa de todo o processo de gravação, incluindo as operações de preparo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11<br/>                                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





