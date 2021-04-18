---
title: Interface IWMPMedia (VB e C) (WMP. h)
description: Fornece uma maneira de definir e recuperar as propriedades de um item de mídia. A interface IWMPMedia expõe as propriedades a seguir.
ms.assetid: 4f67336e-d1d3-4f18-b063-086edf9d9094
keywords:
- IWMPMedia (VB e C) interface do Windows Media Player
- IWMPMedia (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPMedia (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c60a3396710ea4c426bd41c96db34e1e59cc690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760252"
---
# <a name="iwmpmedia-vb-and-c-interface"></a>Interface IWMPMedia (VB e C#)

Fornece uma maneira de definir e recuperar as propriedades de um item de mídia.

A interface **IWMPMedia** expõe as propriedades a seguir.

## <a name="members"></a>Membros

A interface **IWMPMedia (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IWMPMedia (VB e C#)** tem esses métodos.



| Método                                                                             | Descrição                                                                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**GetAttributeName**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)   | Retorna o nome do atributo correspondente ao índice especificado.<br/>                            |
| [**getItemInfo**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)             | Retorna o valor do atributo especificado para o item de mídia.<br/>                                   |
| [**getItemInfoByAtom**](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md) | Retorna o valor do atributo com o número de índice especificado.<br/>                                |
| [**Getmarkname**](wmplibiwmpmedia-iwmpmedia-getmarkername--vb-and-c.md)         | Retorna o nome do marcador no índice especificado.<br/>                                             |
| [**getmarcadortime**](wmplibiwmpmedia-iwmpmedia-getmarkertime--vb-and-c.md)         | Retorna a hora do marcador no índice especificado.<br/>                                             |
| [**isMemberOf**](wmplibiwmpmedia-iwmpmedia-ismemberof--vb-and-c.md)               | Retorna um valor que indica se o item de mídia especificado é um membro da playlist especificada.<br/> |
| [**isReadOnlyItem**](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)       | Retorna um valor que indica se os atributos do item de mídia especificado podem ser editados.<br/>       |
| [**setItemInfo**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)             | Define o valor do atributo especificado para o item de mídia.<br/>                                      |



 

### <a name="properties"></a>Propriedades

A interface **IWMPMedia (VB e C#)** tem essas propriedades.



| Propriedade                                                                                      | Tipo de acesso          | Descrição                                                                                                                                          |
|:----------------------------------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attributeCount**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)<br/>       | Somente leitura<br/> | Obtém o número de atributos que podem ser consultados e/ou definidos para o item de mídia.<br/>                                                          |
| [**permanência**](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)<br/>                   | Somente leitura<br/> | Obtém a duração em segundos do item de mídia atual.<br/>                                                                                   |
| [**duraçãostring**](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)<br/>       | Somente leitura<br/> | Obtém um valor que indica a duração do item de mídia atual no formato HH: MM: SS.<br/>                                                        |
| [**imageSourceHeight**](wmplibiwmpmedia-iwmpmedia-imagesourceheight--vb-and-c.md)<br/> | Somente leitura<br/> | Obtém a altura do item de mídia atual em pixels.<br/>                                                                                      |
| [**imageSourceWidth**](wmplibiwmpmedia-iwmpmedia-imagesourcewidth--vb-and-c.md)<br/>   | Somente leitura<br/> | Obtém a largura do item de mídia atual em pixels.<br/>                                                                                       |
| [**isidêntico**](iwmpmedia-isidentical--vb-and-c.md)<br/>                             | Somente leitura<br/> | Obtém um valor que indica se o item de mídia especificado é o mesmo que o atual. No C#, esse é o método **Get \_ isidêntico** .<br/> |
| [**markerCount**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)<br/>             | Somente leitura<br/> | Obtém o número de marcadores no item de mídia.<br/>                                                                                             |
| [**nomes**](wmplibiwmpmedia-iwmpmedia-name--vb-and-c.md)<br/>                           | Somente leitura<br/> | Obtém ou define o nome do item de mídia.<br/>                                                                                                  |
| [**sourceURL**](wmplibiwmpmedia-iwmpmedia-sourceurl--vb-and-c.md)<br/>                 | Somente leitura<br/> | Obtém a URL do item de mídia.<br/>                                                                                                           |



 

Obtenha uma interface **IWMPMedia** usando as propriedades ou métodos a seguir acessados por meio do objeto ou da interface a seguir.



| Objeto ou interface                                               | Propriedade ou método                                                                                                                       |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMPControls**](iwmpcontrols--vb-and-c.md)                    | [**CurrentItem**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                             |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md), [ **newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md) |
| [**IWMPPlaylist**](iwmpplaylist--vb-and-c.md)                    | [**Item**](iwmpplaylist-item--vb-and-c.md) (obter \_ item em C#)                                                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPMedia2 (VB e C#)**](iwmpmedia2--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia3 (VB e C#)**](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





