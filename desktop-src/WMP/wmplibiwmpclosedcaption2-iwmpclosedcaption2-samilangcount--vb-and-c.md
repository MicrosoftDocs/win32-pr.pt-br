---
title: Propriedade IWMPClosedCaption2 SAMILangCount
description: A propriedade SAMILangCount Obtém o número de idiomas com suporte pelo arquivo SAMI atual.
ms.assetid: e3c7203d-66cb-49e2-9204-795c0f27248f
keywords:
- Windows Media Player da propriedade SAMILangCount
- propriedade SAMILangCount Windows Media Player, interface IWMPClosedCaption2
- Windows Media Player de interface IWMPClosedCaption2, propriedade SAMILangCount
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMILangCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b85ce04bd672f0219b8dd96f91172241689a80042a37a7680e2f8e26b65c85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899996"
---
# <a name="iwmpclosedcaption2samilangcount-property"></a>Propriedade IWMPClosedCaption2:: SAMILangCount

A propriedade **SAMILangCount** Obtém o número de idiomas com suporte pelo arquivo Sami atual.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 SAMILangCount {get; set;}
```


```VB

Public ReadOnly Property SAMILangCount As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é o número de idiomas com suporte.

## <a name="remarks"></a>Comentários

Essa propriedade retorna 0, a menos que um arquivo de mídia digital esteja aberto (AxWindowsMediaPlayer. OpenState é igual a 13).

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

[**IWMPClosedCaption. SAMILang (VB e C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2. getSAMILangName (VB e C#)**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)
</dt> </dl>

 

 





