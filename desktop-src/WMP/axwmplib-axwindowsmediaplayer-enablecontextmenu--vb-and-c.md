---
title: Propriedade AxWindowsMediaPlayer. enableContextMenu
description: A propriedade enableContextMenu Obtém ou define um valor que indica se o menu de contexto deve ser habilitado, que aparece quando o botão direito do mouse é clicado.
ms.assetid: 6096cab7-c1fa-4b71-804b-e84facab2229
keywords:
- Propriedade enableContextMenu Windows Media Player
- Propriedade enableContextMenu Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade enableContextMenu
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.enableContextMenu
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09c705fd45b9b994863ab4f93df1c3ae10858930
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763375"
---
# <a name="axwindowsmediaplayerenablecontextmenu-property"></a>Propriedade AxWindowsMediaPlayer. enableContextMenu

A propriedade enableContextMenu Obtém ou define um valor que indica se o menu de contexto deve ser habilitado, que aparece quando o botão direito do mouse é clicado.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Boolean enableContextMenu {get; set;}
```


```VB

Public Property enableContextMenu As System.Boolean
```





## <a name="property-value"></a>Valor da propriedade

Um valor System. Boolean que indica se o menu de contexto deve ser habilitado. O valor padrão é true.

## <a name="remarks"></a>Comentários

Durante a reprodução de tela inteira, o Windows Media Player oculta o cursor do mouse quando **enableContextMenu** é igual a false e **UIMODE** é igual a "None".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





