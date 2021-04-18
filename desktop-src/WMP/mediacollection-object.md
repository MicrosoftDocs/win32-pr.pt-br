---
title: Objeto mediacollection
description: O objeto Mediacollection fornece uma maneira de organizar uma grande coleção de itens de mídia. Ele pode ser consultado para gerar listas de reprodução automaticamente.
ms.assetid: afcb2c51-3ecb-4529-8f3e-56aa6d0ec2b4
keywords:
- Objeto mediacollection Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2232e3590acd371039494b31c5d592c2e00f0199
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105800121"
---
# <a name="mediacollection-object"></a>Objeto mediacollection

O objeto **mediacollection** fornece uma maneira de organizar uma grande coleção de itens de mídia. Ele pode ser consultado para gerar listas de reprodução automaticamente.

O objeto **mediacollection** dá suporte aos seguintes métodos.



| Método                                                                           | Descrição                                                                                                                                                    |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [add](mediacollection-add.md)                                                   | Adiciona um novo item de mídia ou lista de reprodução à biblioteca.                                                                                                              |
| [createQuery](mediacollection-createquery.md)                                   | Cria um novo objeto de [consulta](query-object.md) .                                                                                                                |
| [getAll](mediacollection-getall.md)                                             | Recupera um objeto [playlist](playlist-object.md) contendo todos os itens de mídia na biblioteca.                                                                  |
| [getAttributeStringCollection](mediacollection-getattributestringcollection.md) | Recupera um objeto [StringCollection](stringcollection-object.md) que representa o conjunto de todos os valores de um atributo especificado dentro de um tipo de mídia especificado. |
| [getByAlbum](mediacollection-getbyalbum.md)                                     | Recupera um objeto [playlist](playlist-object.md) contendo itens de mídia do álbum especificado.                                                            |
| [getByAttribute](mediacollection-getbyattribute.md)                             | Recupera um objeto [playlist](playlist-object.md) contendo itens de mídia com o atributo especificado com o valor especificado.                             |
| [getByAttributeAndMediaType](mediacollection-getbyattributeandmediatype.md)     | Recupera um objeto [playlist](playlist-object.md) contendo objetos de [mídia](media-object.md) com o tipo de mídia e o atributo especificados.                 |
| [getByAuthor](mediacollection-getbyauthor.md)                                   | Recupera um objeto [playlist](playlist-object.md) contendo itens de mídia pelo autor especificado.                                                             |
| [getByGenre](mediacollection-getbygenre.md)                                     | Recupera um objeto [playlist](playlist-object.md) contendo itens de mídia com o gênero especificado.                                                            |
| [getByName](mediacollection-getbyname.md)                                       | Recupera um objeto [playlist](playlist-object.md) contendo itens de mídia com o nome especificado.                                                             |
| [getMediaAtom](mediacollection-getmediaatom.md)                                 | Recupera o índice no qual uma propriedade especificada reside no conjunto de propriedades disponíveis.                                                              |
| [getPlaylistByQuery](mediacollection-getplaylistbyquery.md)                     | Recupera um objeto [playlist](playlist-object.md) contendo objetos de [mídia](media-object.md) que correspondem às condições de consulta.                               |
| [getStringCollectionByQuery](mediacollection-getstringcollectionbyquery.md)     | Recupera um objeto [StringCollection](stringcollection-object.md) que contém cadeias de caracteres que correspondem às condições de consulta.                                         |
| [isDeleted](mediacollection-isdeleted.md)                                       | Recupera um valor que indica se o item de mídia especificado está na pasta itens excluídos.                                                                  |
| [remove](mediacollection-remove.md)                                             | Remove um item da coleção de mídia.                                                                                                                     |
| [setdeled](mediacollection-setdeleted.md)                                     | Move o item de mídia especificado para a pasta itens excluídos.                                                                                                    |



 

O objeto **mediacollection** é acessado por meio da propriedade a seguir.



| Objeto                      | Propriedade                                      |
|-----------------------------|-----------------------------------------------|
| [Jogador](player-object.md) | [mediacollection](player-mediacollection.md) |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




