---
title: Propriedade autoStart de IWMPSettings
description: A propriedade autoStart obtém ou define um valor que indica se o item de mídia atual começa a ser a reprodução automática.
ms.assetid: 01a1cb78-9951-478a-8ea3-1ae06164beab
keywords:
- Propriedade autoStart Windows Media Player
- a propriedade autoStart Windows Media Player interface , IWMPSettings
- Interface IWMPSettings Windows Media Player , propriedade autoStart
topic_type:
- apiref
api_name:
- IWMPSettings.autoStart
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7be64a030bbfe8abbd81830a7638094cd3da93939f3184ad3a4cfca0063c9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568463"
---
# <a name="iwmpsettingsautostart-property"></a>Propriedade IWMPSettings::autoStart

A **propriedade autoStart** obtém ou define um valor que indica se o item de mídia atual começa a ser a reprodução automática.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean autoStart {get; set;}
```


```VB

Public Property autoStart As System.Boolean
```





## <a name="property-value"></a>Valor da propriedade

Um **valor System.Boolean** que indica se o item de mídia atual começa a ser tocando automaticamente. O padrão é **true**.

## <a name="remarks"></a>Comentários

Se **AutoStart** for definido como **true**, o item de mídia começará a ser a reprodução quando **AxWindowsMediaPlayer.URL**, **AxWindowsMediaPlayer.currentPlaylist ou** **AxWindowsMediaPlayer.currentMedia** estiver definido. Caso contrário, o item de mídia não começará a reproduzir até que **o método IWMPControls.play** seja chamado.

A menos que você delimita **autoStart** como **true** imediatamente antes de especificar um item de mídia, você não deve contar com essa configuração como um substituto para usar o **método IWMPControls.play.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AxWindowsMediaPlayer.currentMedia (VB e C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.currentPlaylist (VB e C#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPControls.play (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





