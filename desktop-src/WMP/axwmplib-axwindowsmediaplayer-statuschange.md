---
title: Evento StatusChange do objeto AxWindowsMediaPlayer
description: O evento StatusChange ocorre quando o valor da propriedade status é alterado. | Evento StatusChange do objeto AxWindowsMediaPlayer
ms.assetid: 5295fccb-7be0-46d3-85ba-b481e575d393
keywords:
- Evento StatusChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- StatusChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3ef3224afadb1f98a3067913a8beb095d4e46e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762100"
---
# <a name="statuschange-event-of-the-axwindowsmediaplayer-object"></a>Evento StatusChange do objeto AxWindowsMediaPlayer

O evento **StatusChange** ocorre quando o valor da propriedade **status** é alterado.

``` syntax
[C#]
private void player_StatusChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_StatusChange(
  sender As Object,
  e As System.EventArgs
) Handles player.StatusChange
```

## <a name="event-data"></a>Dados de evento

Este evento não contém dados.

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

[**AxWindowsMediaPlayer. status (VB e C#)**](axwmplib-axwindowsmediaplayer-status--vb-and-c.md)
</dt> </dl>

 

 





