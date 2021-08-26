---
title: Propriedade do rótulo IWMPCdromBurn
description: A propriedade Label Obtém a cadeia de caracteres do rótulo do volume do CD.
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- Windows Media Player de Propriedade do rótulo
- propriedade do rótulo Windows Media Player, interface IWMPCdromBurn
- Windows Media Player de interface IWMPCdromBurn, propriedade label
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
ms.openlocfilehash: d8b8917706e20b5d1361054ac5f6fd209c0026837c428ecba715727e3d828a4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000545"
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

 

 





