---
title: Propriedade do rótulo IWMPCdromBurn
description: A propriedade Label Obtém a cadeia de caracteres do rótulo do volume do CD.
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- Propriedade de rótulo Windows Media Player
- Propriedade de rótulo Windows Media Player, interface IWMPCdromBurn
- Interface IWMPCdromBurn Windows Media Player, Propriedade Label
topic_type:
- apiref
api_name:
- IWMPCdromBurn.label
- IWMPCdromBurn.get_label
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05da344f1148de7e79cb605135964c6ab8225ac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780376"
---
# <a name="iwmpcdromburnlabel-property"></a>Propriedade IWMPCdromBurn:: Label

A propriedade *Label* Obtém a cadeia de caracteres do rótulo do volume do CD.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String label {get;}
```


```VB

Public ReadOnly Property label As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um **System. String** que é a cadeia de caracteres do rótulo do volume.

## <a name="remarks"></a>Comentários

Devido à maneira como os rótulos de CD são armazenados, o rótulo do CD pode ser menor do que o comprimento da cadeia de caracteres do rótulo de volume especificado. Se a cadeia de caracteres for maior do que o comprimento máximo de um rótulo de CD, o texto será truncado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





