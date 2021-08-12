---
title: Interface IWMPPlaylistCollection (VB e C) (WMP. h)
description: Fornece métodos para manipular interfaces IWMPPlaylist e IWMPPlaylistArray em uma coleção.
ms.assetid: 19a4e0d7-cb3f-42ec-9acb-7ac0c5837662
keywords:
- Windows Media Player de interface IWMPPlaylistCollection (VB e C)
- Windows Media Player de interface IWMPPlaylistCollection (VB e C), descrita
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection (VB and C )
- IWMPPlaylistCollection (VB and C ).setDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ae130b9134d9ad6e19fa062946a591cdf7749b428201750fda8ff55252c3212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575212"
---
# <a name="iwmpplaylistcollection-vb-and-c-interface"></a>Interface IWMPPlaylistCollection (VB e C#)

Fornece métodos para manipular interfaces **IWMPPlaylist** e **IWMPPlaylistArray** em uma coleção.

## <a name="members"></a>Membros

A interface **IWMPPlaylistCollection (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMPPlaylistCollection (VB e C#)** tem esses métodos.



| Método                                                                                                 | Descrição                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**getAll**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)                 | Retorna uma interface **IWMPPlaylistArray** que fornece acesso a todas as listas de reprodução na biblioteca.<br/>             |
| [**getByName**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)           | Retorna uma interface **IWMPPlaylistArray** que fornece acesso a listas de reprodução com o nome especificado, se existir.<br/> |
| [**importPlaylist**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md) | Adiciona uma lista de reprodução estática à biblioteca.<br/>                                                                              |
| [**isDeleted**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-isdeleted--vb-and-c.md)           | Retorna um valor que indica se a playlist especificada está na pasta itens excluídos.<br/>                           |
| [**newPlaylist**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)       | Retorna uma interface **IWMPPlaylist** para uma lista de reprodução nova e vazia na biblioteca.<br/>                                     |
| [**exclu**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-remove--vb-and-c.md)                 | Remove uma lista de reprodução da biblioteca.<br/>                                                                                |
| **setdeled**                                                                                         | Não tem mais suporte.<br/>                                                                                                |



 

Obtenha uma interface **IWMPPlaylistCollection** usando a propriedade a seguir.



| Objeto                                                                   | Propriedade                                                                                 |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**playlistcollection**](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .net e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylistArray (VB e C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





