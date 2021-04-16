---
title: Propriedade AutoStart do IWMPSettings
description: A propriedade AutoStart Obtém ou define um valor que indica se o item de mídia atual começa a ser reproduzido automaticamente.
ms.assetid: 01a1cb78-9951-478a-8ea3-1ae06164beab
keywords:
- Propriedade AutoStart do Windows Media Player
- Propriedade AutoStart do Windows Media Player, interface IWMPSettings
- Interface IWMPSettings do Windows Media Player, Propriedade AutoStart
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
ms.openlocfilehash: aaf6c1fb43107df11462737286e26fa7801360d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765359"
---
# <a name="iwmpsettingsautostart-property"></a>Propriedade IWMPSettings:: AutoStart

A propriedade **AutoStart** Obtém ou define um valor que indica se o item de mídia atual começa a ser reproduzido automaticamente.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean autoStart {get; set;}
```


```VB

Public Property autoStart As System.Boolean
```





## <a name="property-value"></a>Valor da propriedade

Um valor **System. Boolean** que indica se o item de mídia atual começa a ser reproduzido automaticamente. O padrão é **true**.

## <a name="remarks"></a>Comentários

Se **AutoStart** for definido como **true**, o item de mídia começará a ser reproduzido quando **AxWindowsMediaPlayer. URL**, **AxWindowsMediaPlayer. currentPlaylist** ou **AxWindowsMediaPlayer. currentMedia** for definido. Caso contrário, o item de mídia não começará a ser reproduzido até que o método **IWMPControls. Play** seja chamado.

A menos que você defina **AutoStart** como **true** imediatamente antes de especificar um item de mídia, você não deve confiar nessa configuração como um substituto para usar o método **IWMPControls. Play** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AxWindowsMediaPlayer. currentMedia (VB e C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. currentPlaylist (VB e C#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Play (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





