---
title: Evento FolderScanStateChange do objeto AxWindowsMediaPlayer
description: O evento FolderScanStateChange ocorre quando uma operação de monitoramento de pasta altera o estado.
ms.assetid: f68829a3-00df-417a-ae78-49dff1e6f09b
keywords:
- Evento FolderScanStateChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- FolderScanStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3672f16bee5251aa46e6a64a0da983e0f34ec54a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760468"
---
# <a name="folderscanstatechange-event-of-the-axwindowsmediaplayer-object"></a>Evento FolderScanStateChange do objeto AxWindowsMediaPlayer

O evento FolderScanStateChange ocorre quando uma operação de monitoramento de pasta altera o estado.

``` syntax
[C#]
private void player_FolderScanStateChange(
  object sender,
  _WMPOCXEvents_FolderScanStateChangeEvent e
)

[Visual Basic]
Private Sub player_FolderScanStateChange( 
  sender As Object,  
  e As _WMPOCXEvents_FolderScanStateChangeEvent
) Handles player.FolderScanStateChange
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ FolderScanStateChangeEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ FolderScanStateChangeEvent**, que contém a seguinte propriedade relacionada a este evento.



| Propriedade | Descrição                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| wmpfss   | Valor de enumeração WMPLib. WMPFolderScanStateThe que indica o novo estado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11<br/>                                                                                         |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**WMPFolderScanState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpfolderscanstate)
</dt> </dl>

 

 





