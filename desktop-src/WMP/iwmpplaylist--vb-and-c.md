---
title: Interface IWMPPlaylist (VB e C) (Wmp.h)
description: Fornece propriedades e métodos para organizar, gerenciar e manipular itens de mídia em uma lista de reprodução. A interface IWMPPlaylist expõe as propriedades a seguir.
ms.assetid: c3f4f9dd-eb5f-493a-b8d0-22e70c63a2d1
keywords:
- Windows Media Player de interface IWMPPlaylist (VB e C)
- Windows Media Player de interface IWMPPlaylist (VB e C), descrita
topic_type:
- apiref
api_name:
- IWMPPlaylist (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3fc1d8be09596d89dd87748811846d6dee1e8af8f28bebec56fa852c42ed6bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118987"
---
# <a name="iwmpplaylist-vb-and-c-interface"></a>Interface IWMPPlaylist (VB e C#)

Fornece propriedades e métodos para organizar, gerenciar e manipular itens de mídia em uma lista de reprodução.

A interface **IWMPPlaylist** expõe as propriedades a seguir.

## <a name="members"></a>Membros

A interface **IWMPPlaylist (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IWMPPlaylist (VB e C#)** tem esses métodos.



| Método                                                                       | Descrição                                                             |
|:-----------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**appendItem**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)   | Adiciona um item de mídia ao final da lista de reprodução.<br/>                |
| [**formatação**](iwmpplaylist-iwmpplaylist-clear--vb-and-c.md)                   | Reservado para uso futuro.<br/>                                     |
| [**getItemInfo**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) | Retorna o valor de um atributo de playlist especificado pelo nome.<br/> |
| [**insertItem**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)   | Insere um item de mídia em um local especificado em uma lista de reprodução.<br/>  |
| [**moveItem**](wmplibiwmpplaylist-iwmpplaylist-moveitem--vb-and-c.md)       | Altera o local de um item de mídia na lista de reprodução.<br/>        |
| [**removeItem**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)   | Remove o item de mídia especificado da lista de reprodução.<br/>          |
| [**setItemInfo**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md) | Define o valor de um atributo de playlist.<br/>                      |



 

### <a name="properties"></a>Propriedades

A interface **IWMPPlaylist (VB e C#)** tem essas propriedades.



| Propriedade                                                                                      | Tipo de acesso           | Descrição                                                                                                                                         |
|:----------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attributeCount**](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)<br/> | Somente leitura<br/>  | Obtém o número de atributos associados a uma lista de reprodução.<br/>                                                                                |
| [**attributeName**](iwmpplaylist-attributename--vb-and-c.md)<br/>                      | Somente leitura<br/>  | Obtém o nome de um atributo de playlist especificado por um índice. Em C#, este é o \_ método Get AttributeName.<br/>                               |
| [**contar**](wmplibiwmpplaylist-iwmpplaylist-count--vb-and-c.md)<br/>                   | Somente leitura<br/>  | Obtém o número de itens de mídia em uma lista de reprodução.<br/>                                                                                            |
| [**isidêntico**](iwmpplaylist-isidentical--vb-and-c.md)<br/>                          | Somente leitura<br/>  | Obtém um valor que indica se a playlist especificada é idêntica à playlist atual. Em C#, esse é o \_ método Get isidêntico.<br/> |
| [**Item**](iwmpplaylist-item--vb-and-c.md)<br/>                                        | Somente leitura<br/>  | Obtém uma interface para o item de mídia no índice especificado. Em C#, esse é o \_ método get item.<br/>                                         |
| [**nomes**](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)<br/>                     | Leitura/gravação<br/> | Obtém ou define o nome da lista de reprodução.<br/>                                                                                                   |



 

Obtenha uma interface **IWMPPlaylist** usando as propriedades ou métodos a seguir acessados por meio do objeto ou da interface a seguir.



| Objeto ou interface                                                | Propriedade ou método                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMPCdrom**](iwmpcdrom--vb-and-c.md)                           | [**Playlist**](wmplibiwmpcdrom-iwmpcdrom-playlist--vb-and-c.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**IWMPMediaCollection**](iwmpmediacollection--vb-and-c.md)       | [**getAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md), [**getByAlbum**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum), [**getByAttribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md), [**getByAuthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md), [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md), [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md) |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md)  | [**currentPlaylist**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md), [ **newPlaylist**](axwmplib-axwindowsmediaplayer-newplaylist.md)                                                                                                                                                                                                                                                                                                                                                                   |
| [**IWMPPlaylistArray**](iwmpplaylistarray--vb-and-c.md)           | [**Item**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistarray-item)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**IWMPPlaylistCollection**](iwmpplaylistcollection--vb-and-c.md) | [**newPlaylist**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-newplaylist)                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .net e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





