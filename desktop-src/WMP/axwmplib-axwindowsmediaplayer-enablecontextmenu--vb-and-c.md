---
title: Propriedade AxWindowsMediaPlayer. enableContextMenu
description: A propriedade enableContextMenu Obtém ou define um valor que indica se o menu de contexto deve ser habilitado, que aparece quando o botão direito do mouse é clicado.
ms.assetid: 6096cab7-c1fa-4b71-804b-e84facab2229
keywords:
- Windows Media Player da propriedade enableContextMenu
- propriedade enableContextMenu Windows Media Player, classe AxWindowsMediaPlayer
- classe AxWindowsMediaPlayer Windows Media Player, propriedade enableContextMenu
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
ms.openlocfilehash: 5603762ec9823f7e9896c5c22c1dee33f2399bb02301921057f8502046bcc002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582335"
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

durante a reprodução de tela inteira, Windows Media Player oculta o cursor do mouse quando **enableContextMenu** é igual a false e **uiMode** é igual a "none".

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

 

 





