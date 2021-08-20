---
title: Propriedade IWMPClosedCaption captioningId
description: A propriedade IWMPClosedCaption Obtém ou define o nome do elemento HTML que exibe a legenda.
ms.assetid: b09bb7c7-c3b6-4e0d-962f-24b06a04f6d1
keywords:
- Windows Media Player da propriedade captioningId
- propriedade captioningId Windows Media Player, interface IWMPClosedCaption
- Windows Media Player de interface IWMPClosedCaption, propriedade captioningId
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
ms.openlocfilehash: 45f6d4c10beb3f0fd94da0365d67b6c5ab480d36d5a3786021f538e9dcf4e90c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116052"
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

O nome do elemento especificado pode ser qualquer elemento HTML na página da Web, contanto que dê suporte ao atributo **InnerHtml** . se a página da web contiver vários quadros, o nome do elemento só poderá fazer referência a um elemento no mesmo quadro que o controle de Windows Media Player.

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

 

 





