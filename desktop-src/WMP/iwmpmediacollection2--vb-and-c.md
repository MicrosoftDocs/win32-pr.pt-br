---
title: Interface IWMPMediaCollection2 (VB e C) (WMP. h)
description: Fornece métodos que complementam a interface IWMPMediaCollection.
ms.assetid: 204f336c-ea78-43d4-9686-bcab72362bc9
keywords:
- IWMPMediaCollection2 (VB e C) interface do Windows Media Player
- IWMPMediaCollection2 (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPMediaCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58175e80fbf0f706a9ae6c6b3b69afbd26d52af3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789536"
---
# <a name="iwmpmediacollection2-vb-and-c-interface"></a>Interface IWMPMediaCollection2 (VB e C#)

Fornece métodos que complementam a interface **IWMPMediaCollection** .

## <a name="members"></a>Membros

A interface **IWMPMediaCollection2 (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMPMediaCollection2 (VB e C#)** tem esses métodos.



| Método                                                                                                                     | Descrição                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**createQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)                               | Retorna uma interface **IWMPQuery** que representa uma nova consulta.<br/>                                                                                               |
| [**getByAttributeAndMediaType**](wmplibiwmpmediacollection2-iwmpmediacollection2-getbyattributeandmediatype--vb-and-c.md) | Retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia que têm um tipo de mídia e um atributo especificado.<br/>                                     |
| [**getPlaylistByQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)                 | Retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia que correspondem às condições de consulta.<br/>                                                    |
| [**getStringCollectionByQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md) | Retorna uma interface **IWMPStringCollection** que fornece acesso ao conjunto de todos os valores de cadeia de caracteres para um atributo especificado que corresponde às condições de consulta.<br/> |



 

Obtenha uma interface **IWMPMediaCollection2** convertendo o valor retornado pela propriedade [**AxWindowsMediaPlayer. mediacollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) ou o valor retornado pela propriedade [**IWMPLibrary. mediacollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





