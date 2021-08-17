---
title: Interface IWMPMediaCollection (VB e C) (WMP. h)
description: Fornece métodos que podem ser usados para organizar uma grande coleção de itens de mídia.
ms.assetid: a9e3d466-7dcf-4f1b-ba6f-9d166a35f03d
keywords:
- Windows Media Player de interface IWMPMediaCollection (VB e C)
- Windows Media Player de interface IWMPMediaCollection (VB e C), descrita
topic_type:
- apiref
api_name:
- IWMPMediaCollection (VB and C )
- IWMPMediaCollection (VB and C ).isDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce15616b2059802610360b52d5af9bfa8d56b56b7ed06129bb849de567e22e26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468446"
---
# <a name="iwmpmediacollection-vb-and-c-interface"></a>Interface IWMPMediaCollection (VB e C#)

Fornece métodos que podem ser usados para organizar uma grande coleção de itens de mídia.

## <a name="members"></a>Membros

A interface **IWMPMediaCollection (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMPMediaCollection (VB e C#)** tem esses métodos.



| Método                                                                                                                       | Descrição                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**add**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)                                                   | Adiciona um novo item de mídia ou lista de reprodução à biblioteca.<br/>                                                                                  |
| [**getAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md)                                             | Retorna uma interface **IWMPPlaylist** que corresponde à playlist que contém todos os itens de mídia na biblioteca.<br/>               |
| [**getAttributeStringCollection**](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md) | Retorna uma interface **IWMPStringCollection** que representa o conjunto de todos os valores de um atributo especificado dentro de um tipo de mídia.<br/> |
| [**getByAlbum**](wmplibiwmpmediacollection-iwmpmediacollection-getbyalbum--vb-and-c.md)                                     | Retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia do álbum especificado.<br/>                                |
| [**getByAttribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md)                             | Retorna uma interface **IWMPPlaylist** que corresponde ao atributo especificado com o valor especificado.<br/>                      |
| [**getByAuthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md)                                   | Retorna uma interface **IWMPPlaylist** que fornece acesso aos itens de mídia pelo autor especificado.<br/>                             |
| [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md)                                     | Retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia do gênero especificado.<br/>                                  |
| [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)                                       | Retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia com o nome especificado.<br/>                                 |
| [**getMediaAtom**](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)                                 | Retorna o índice de um atributo especificado.<br/>                                                                                        |
| **isDeleted**                                                                                                                | Não tem mais suporte.<br/>                                                                                                               |
| [**exclu**](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)                                             | Remove o item de mídia especificado da coleção de mídia.<br/>                                                                        |
| [**setdeled**](wmplibiwmpmediacollection-iwmpmediacollection-setdeleted--vb-and-c.md)                                     | Move o item de mídia especificado para a pasta itens excluídos.<br/>                                                                        |



 

Obtenha uma interface **IWMPMediaCollection** usando as seguintes propriedades acessadas por meio do objeto ou da interface a seguir.



| Objeto ou interface                                               | Propriedade                                                                           |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**mediacollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) |
| [**IWMPLibrary**](iwmplibrary--vb-and-c.md)                      | [**mediacollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .net e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPMediaCollection2**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interface IWMPStringCollection (VB e C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





