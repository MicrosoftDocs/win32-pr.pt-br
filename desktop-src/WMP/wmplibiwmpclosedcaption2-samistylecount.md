---
title: Propriedade IWMPClosedCaption2 SAMIStyleCount
description: A propriedade SAMIStyleCount obtém o número de estilos com suporte pelo arquivo SAMI atual.
ms.assetid: e2a0d194-6fa2-48c9-9fc7-0b60029d2e5d
keywords:
- Propriedade SAMIStyleCount Windows Media Player
- A propriedade SAMIStyleCount Windows Media Player , interface IWMPClosedCaption2
- Interface IWMPClosedCaption2 Windows Media Player , propriedade SAMIStyleCount
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMIStyleCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f73ab4e252386f790f74741053012239d0219b1e296e392146894f906e1556f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115913"
---
# <a name="iwmpclosedcaption2samistylecount-property"></a>Propriedade IWMPClosedCaption2::SAMIStyleCount

A **propriedade SAMIStyleCount** obtém o número de estilos com suporte pelo arquivo SAMI atual.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 SAMIStyleCount {get; set;}
```


```VB

Public ReadOnly Property SAMIStyleCount As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System.Int32** que é o número de estilos.

## <a name="remarks"></a>Comentários

Essa propriedade retorna 0, a menos que um arquivo de mídia digital esteja aberto (AxWindowsMediaPlayer.openState é igual a 13).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas fechadas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interface IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption.SAMIStyle (VB e C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2.getSAMIStyleName (VB e C#)**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamistylename--vb-and-c.md)
</dt> </dl>

 

 





