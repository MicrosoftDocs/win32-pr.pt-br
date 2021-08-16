---
title: Propriedade AxWindowsMediaPlayer. openState
description: A propriedade OpenState Obtém um valor de enumeração que indica o estado da fonte de conteúdo.
ms.assetid: 7a76814a-649f-4516-a92a-5f536fb1b147
keywords:
- Windows Media Player da propriedade openState
- propriedade openstate Windows Media Player, classe AxWindowsMediaPlayer
- classe AxWindowsMediaPlayer Windows Media Player, propriedade openstate
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
ms.openlocfilehash: 09fa09451bf323a9f30afeddf7b2d003183a1eba7b0999a79fb42c70e1417013
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573566"
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

não há garantia de que os estados de Windows Media Player ocorram em uma ordem específica. Além disso, nem todo estado ocorre necessariamente durante uma sequência de eventos. Você não deve escrever código que dependa da ordem de estado.

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

 

 





