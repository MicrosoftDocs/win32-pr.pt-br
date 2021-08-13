---
title: Interface IWMPMedia3 (VB e C) (WMP. h)
description: Fornece métodos adicionais para acessar as propriedades de um item de mídia.
ms.assetid: e16aa5e2-ae44-41c2-8c61-fb688c2e89e2
keywords:
- Windows Media Player de interface IWMPMedia3 (VB e C)
- Windows Media Player de interface IWMPMedia3 (VB e C), descrita
topic_type:
- apiref
api_name:
- IWMPMedia3 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d536f792f0acc8003669be05448ec1f68f82830ccbadf75483bbbc6b84610ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415908"
---
# <a name="iwmpmedia3-vb-and-c-interface"></a>Interface IWMPMedia3 (VB e C#)

Fornece métodos adicionais para acessar as propriedades de um item de mídia.

## <a name="members"></a>Membros

A interface **IWMPMedia3 (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMPMedia3 (VB e C#)** tem esses métodos.



| Método                                                                                           | Descrição                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**getAttributeCountByType**](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md) | Retorna o número de atributos associados ao tipo de atributo especificado.<br/>              |
| [**getItemInfoByType**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)             | Retorna o valor do atributo correspondente ao tipo de atributo e ao índice especificados.<br/> |



 

Obtenha uma interface **IWMPMedia3** convertendo o valor retornado por uma das propriedades ou métodos a seguir acessados por meio do objeto ou da interface a seguir.



| Objeto ou interface                                               | Propriedade ou método                                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [IWMPControls](iwmpcontrols--vb-and-c.md)                        | [currentItem](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                          |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md) |
| [IWMPPlaylist](iwmpplaylist--vb-and-c.md)                        | [Item](iwmpplaylist-item--vb-and-c.md) ( **obter \_ Item** em C#)                                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .net e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia2 (VB e C#)**](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





