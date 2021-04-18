---
title: Propriedade IWMPClosedCaption captioningId
description: A propriedade IWMPClosedCaption Obtém ou define o nome do elemento HTML que exibe a legenda.
ms.assetid: b09bb7c7-c3b6-4e0d-962f-24b06a04f6d1
keywords:
- Propriedade captioningId Windows Media Player
- Propriedade captioningId Windows Media Player, interface IWMPClosedCaption
- Interface IWMPClosedCaption Windows Media Player, Propriedade captioningId
topic_type:
- apiref
api_name:
- IWMPClosedCaption.captioningId
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343234fce2b93ac02255731a38025f6d7b9fac6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748669"
---
# <a name="iwmpclosedcaptioncaptioningid-property"></a>Propriedade IWMPClosedCaption:: captioningId

A propriedade **IWMPClosedCaption** Obtém ou define o nome do elemento HTML que exibe a legenda.

## <a name="syntax"></a>Syntax


```CSharp
public System.String captioningId {get; set;}
```


```VB

Public Property captioningId As System.String
```





## <a name="property-value"></a>Valor da propriedade

O **System. String** que é a ID do elemento HTML.

## <a name="remarks"></a>Comentários

O nome do elemento especificado pode ser qualquer elemento HTML na página da Web, contanto que dê suporte ao atributo **InnerHtml** . Se a página da Web contiver vários quadros, o nome do elemento só poderá fazer referência a um elemento no mesmo quadro que o controle do Windows Media Player.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas ocultas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interface IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





