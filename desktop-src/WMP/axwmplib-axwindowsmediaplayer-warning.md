---
title: Evento de aviso do objeto AxWindowsMediaPlayer
description: O evento Warning é reservado para uso futuro.
ms.assetid: 3de63756-2726-4864-8988-fd614f23bcad
keywords:
- Evento de aviso do objeto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- Warning Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18925236148a508e66bb34e83f7ddb69f0cb59d87c98dfe0188f780ea2fc3605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003996"
---
# <a name="warning-event-of-the-axwindowsmediaplayer-object"></a>Evento de aviso do objeto AxWindowsMediaPlayer

O evento Warning é reservado para uso futuro.

``` syntax
[C#]
private void player_Warning(
  object sender,
  _WMPOCXEvents_WarningEvent e
)

[Visual Basic]
Private Sub player_Warning(
  sender As Object,
  e As _WMPOCXEvents_WarningEvent
) Handles player.Warning
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ Aviso WMPOCXEventsEventHandler \_**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ WarningEvent**, que contém as propriedades a seguir relacionadas a esse evento.



| Propriedade    | Descrição                                |
|-------------|--------------------------------------------|
| warningType | **System.Int32** Sem suporte.<br/>  |
| param       | **System.Int32** Sem suporte.<br/>  |
| descrição | **System.String** Sem suporte.<br/> |



 

## <a name="remarks"></a>Comentários

Esse evento é reservado para uso futuro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





