---
title: Método playlistcollection. newPlaylist
description: O método newPlaylist cria uma nova lista de reprodução na biblioteca.
ms.assetid: 428b5779-4dc0-466b-9834-6b2c43324013
keywords:
- método newPlaylist Windows Media Player
- método newPlaylist Windows Media Player, classe Playlistcollection
- Classe playlistcollection Windows Media Player, método newPlaylist
topic_type:
- apiref
api_name:
- PlaylistCollection.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d94c25a8dfe6f1eb7c4dac40dd644433a5f0d7e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813673"
---
# <a name="playlistcollectionnewplaylist-method"></a>Método playlistcollection. newPlaylist

O método **newPlaylist** cria uma nova lista de reprodução na biblioteca.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = PlaylistCollection.newPlaylist(
  name
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome da lista de reprodução a ser criada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um objeto **playlist** .

## <a name="remarks"></a>Comentários

Esse método cria uma lista de reprodução vazia na biblioteca. Para preencher a lista de reprodução com itens de mídia, use a *lista de reprodução*. **appendItem** ou *playlist*. **insertItem**.

Várias listas de reprodução com o mesmo nome são permitidas na biblioteca. Para evitar a criação de um nome de playlist duplicado com esse método, use **getByName** e *PlaylistArray*. **contagem** para determinar se já existe uma lista de reprodução com um nome específico.

Espaços à esquerda e à direita não são permitidos em nomes de playlist e são removidos automaticamente do valor especificado para o parâmetro de *nome* .

Para usar esse método, é necessário ter acesso completo à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir cria uma nova lista de reprodução vazia chamada "Trêslist". O objeto de **jogador** foi criado com ID = "Player".


```JScript
//Add a new empty playlist, named ThreeList, to the playlist collection.
var NewList = Player.playlistCollection.newPlaylist("ThreeList");

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Mediacollection. adicionar**](mediacollection-add.md)
</dt> <dt>

[**Playlist. appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Playlist. insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Contagem de PlaylistArray.**](playlistarray-count.md)
</dt> <dt>

[**Objeto playlistcollection**](playlistcollection-object.md)
</dt> <dt>

[**Playlistcollection. getByName**](playlistcollection-getbyname.md)
</dt> <dt>

[**Playlistcollection. importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**Playlistcollection. Remove**](playlistcollection-remove.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





