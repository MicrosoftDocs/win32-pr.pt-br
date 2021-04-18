---
title: Propriedade AxWindowsMediaPlayer. PlayState
description: A propriedade PlayState Obtém um valor de enumeração que indica o estado da operação do Windows Media Player.
ms.assetid: ab9f1547-5c28-4289-beaf-9262f7f59b07
keywords:
- Propriedade PlayState do Windows Media Player
- Propriedade PlayState Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade PlayState
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.playState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d397c65c1cfd7f4adb040cc94e208a66c6c42d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760466"
---
# <a name="axwindowsmediaplayerplaystate-property"></a>Propriedade AxWindowsMediaPlayer. PlayState

A propriedade PlayState Obtém um valor de enumeração que indica o estado da operação do Windows Media Player.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public WMPPlayState playState {get;}
```


```VB

Public ReadOnly Property playState As WMPPlayState
```





## <a name="property-value"></a>Valor da propriedade

O valor de enumeração WMPLib. WMPPlayState.

## <a name="remarks"></a>Comentários

Não há garantia de que os Estados do Windows Media Player ocorram em uma ordem específica. Além disso, nem todo estado ocorre necessariamente durante uma sequência de eventos. Você não deve escrever código que dependa da ordem de estado.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa a propriedade PlayState para exibir o status de execução atual do Player em um rótulo. O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.


```CSharp
// Test whether Windows Media Player is in the playing state. 
if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
{
    playStateLabel.Text = "Windows Media Player is playing!";
}
else
{
    playStateLabel.Text = "Windows Media Player is NOT playing!";
}
```


```VB

' Test whether Windows Media Player is in the playing state. 
If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

    playStateLabel.Text = &quot;Windows Media Player is playing!&quot;

Else

    playStateLabel.Text = &quot;Windows Media Player is NOT playing!&quot;

End If
```





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

[**Evento AxWindowsMediaPlayer. PlayStateChange (VB e C#)**](axwmplib-axwindowsmediaplayer-playstatechange.md)
</dt> <dt>

[**WMPPlayState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 





