---
title: Método playlistcollection. getByName
description: O método getByName recupera um objeto PlaylistArray contendo listas de reprodução com o nome especificado, se existir.
ms.assetid: 0308a98d-1149-4367-b602-33fa54c1760f
keywords:
- Windows Media Player do método getByName
- método getByName Windows Media Player, classe playlistcollection
- classe playlistcollection Windows Media Player, método getByName
topic_type:
- apiref
api_name:
- PlaylistCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 300307ff011abf8b28c645901422291ccab4cf7c66a7a3ba81121ffe1c22e573
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334637"
---
# <a name="playlistcollectiongetbyname-method"></a>Método playlistcollection. getByName

O método **getByName** recupera um objeto **PlaylistArray** contendo listas de reprodução com o nome especificado, se existir.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = PlaylistCollection.getByName(
  name
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome das listas de reprodução a serem recuperadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um objeto **PlaylistArray** .

## <a name="remarks"></a>Comentários

Use *PlaylistArray*. **contagem** para determinar se existe uma lista de reprodução. Se **Count** for zero, uma playlist não existirá.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

o exemplo a seguir JScript usa *playlistcollection*. **getByName** para verificar o objeto **playlistcollection** de uma lista de reprodução chamada "trêslist". Se a lista de reprodução de "três listas" existir, **getByName** definirá "3list" como a playlist atual. O objeto de **jogador** foi criado com a ID = "Player".


```JScript
//Retrieve the count of the playlists named "ThreeList".
var Checkit = Player.playlistCollection.getByName("ThreeList").count;

//Since duplicate playlist names are allowed, the count returned
//will be either zero (no playlist) or greater than zero 
//(playlist exists).
if (Checkit > 0){ 
    
   //Retrieve a playlistArray object containing "ThreeList". Assume that
   //there is only one playlist with that name, and assign it to the 
   //current playlist.
   Player.currentPlaylist = Player.playlistCollection.getByName("ThreeList").item(0);
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**Contagem de PlaylistArray.**](playlistarray-count.md)
</dt> <dt>

[**Objeto playlistcollection**](playlistcollection-object.md)
</dt> <dt>

[**Configurações. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





