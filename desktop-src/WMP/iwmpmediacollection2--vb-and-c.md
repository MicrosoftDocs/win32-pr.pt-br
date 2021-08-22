---
title: Interface IWMPMediaCollection2 (VB e C) (Wmp.h)
description: Fornece métodos que complementam a interface IWMPMediaCollection.
ms.assetid: 204f336c-ea78-43d4-9686-bcab72362bc9
keywords:
- Interface IWMPMediaCollection2 (VB e C) Windows Media Player
- Interface IWMPMediaCollection2 (VB e C ) Windows Media Player , descrita
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
ms.openlocfilehash: 725580d504d07ecc311c89b0ba3121f4f0f62990fcd1cfb6e92cdcbbd3535a55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508736"
---
# <a name="iwmpmediacollection2-vb-and-c-interface"></a>Interface IWMPMediaCollection2 (VB e C#)

Fornece métodos que complementam a interface **IWMPMediaCollection.**

## <a name="members"></a>Membros

A interface **IWMPMediaCollection2 (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMPMediaCollection2 (VB e C#)** tem esses métodos.



| Método                                                                                                                     | Descrição                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Createquery**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)                               | Retorna uma **interface IWMPQuery** que representa uma nova consulta.<br/>                                                                                               |
| [**getByAttributeAndMediaType**](wmplibiwmpmediacollection2-iwmpmediacollection2-getbyattributeandmediatype--vb-and-c.md) | Retorna uma **interface IWMPPlaylist** que fornece acesso a itens de mídia que têm um atributo e um tipo de mídia especificados.<br/>                                     |
| [**getPlaylistByQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)                 | Retorna uma **interface IWMPPlaylist** que fornece acesso a itens de mídia que corresponderem às condições de consulta.<br/>                                                    |
| [**getStringCollectionByQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md) | Retorna uma interface **IWMPStringCollection** que fornece acesso ao conjunto de todos os valores de cadeia de caracteres para um atributo especificado que corresponder às condições de consulta.<br/> |



 

Obter uma interface **IWMPMediaCollection2,** lançando o valor retornado pela propriedade [**AxWindowsMediaPlayer.mediaCollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) ou o valor retornado pela [**propriedade IWMPLibrary.mediaCollection.**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





