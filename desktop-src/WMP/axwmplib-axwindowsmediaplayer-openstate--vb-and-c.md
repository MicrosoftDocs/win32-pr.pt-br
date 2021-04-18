---
title: Propriedade AxWindowsMediaPlayer. openState
description: A propriedade OpenState Obtém um valor de enumeração que indica o estado da fonte de conteúdo.
ms.assetid: 7a76814a-649f-4516-a92a-5f536fb1b147
keywords:
- Propriedade OpenState Windows Media Player
- Propriedade OpenState Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade openState
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 919bf906ce67793c4cd26f32892eae8acf441295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784914"
---
# <a name="axwindowsmediaplayeropenstate-property"></a>Propriedade AxWindowsMediaPlayer. openState

A propriedade OpenState Obtém um valor de enumeração que indica o estado da fonte de conteúdo.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public WMPOpenState openState {get;}
```


```VB

Public ReadOnly Property openState As WMPOpenState
```





## <a name="property-value"></a>Valor da propriedade

O valor de enumeração WMPLib. WMPOpenState.

## <a name="remarks"></a>Comentários

Não há garantia de que os Estados do Windows Media Player ocorram em uma ordem específica. Além disso, nem todo estado ocorre necessariamente durante uma sequência de eventos. Você não deve escrever código que dependa da ordem de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Evento AxWindowsMediaPlayer. OpenStateChange**](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[**WMPLib.WMPOpenState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> </dl>

 

 





