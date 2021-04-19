---
title: Interface IWMPMedia2 (VB e C) (WMP. h)
description: Fornece acesso a uma propriedade de item de mídia adicional.
ms.assetid: 7d9f8304-ae26-4175-b9d4-9f272861ef87
keywords:
- IWMPMedia2 (VB e C) interface do Windows Media Player
- IWMPMedia2 (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPMedia2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1a77322e0e6649d9a286c920ccd9ddc77890f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810546"
---
# <a name="iwmpmedia2-vb-and-c-interface"></a>Interface IWMPMedia2 (VB e C#)

Fornece acesso a uma propriedade de item de mídia adicional.

Além das propriedades e métodos herdados de **IWMPMedia**, a interface **IWMPMedia2** expõe a propriedade a seguir.



| Propriedade                                                 | Descrição                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------|
| [Erro](wmplibiwmpmedia2-iwmpmedia2-error--vb-and-c.md) | Obtém uma interface **IWMPErrorItem** se o item de mídia tiver uma condição de erro. |



 

Obtenha uma interface **IWMPMedia2** convertendo o valor retornado por uma das propriedades ou métodos a seguir acessados por meio do objeto ou da interface a seguir.



| Objeto ou interface                                               | Propriedade ou método                                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [IWMPControls](iwmpcontrols--vb-and-c.md)                        | [currentItem](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                          |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md) |
| [IWMPPlaylist](iwmpplaylist--vb-and-c.md)                        | [Item](iwmpplaylist-item--vb-and-c.md) ( **obter \_ Item** em C#)                                                                   |



 

## <a name="members"></a>Membros

A interface **IWMPMedia2 (VB e C#)** não define nenhum membro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPErrorItem (VB e C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia3 (VB e C#)**](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





