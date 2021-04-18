---
title: Método mediacollection. getByAlbum
description: O método GetByAlbum recupera uma lista de reprodução que contém os itens de mídia do álbum especificado.
ms.assetid: e7e72f0e-e0ae-4bbd-a8b7-966f0fc50059
keywords:
- método getByAlbum Windows Media Player
- método getByAlbum Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método getByAlbum
topic_type:
- apiref
api_name:
- MediaCollection.getByAlbum
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d94cdfa880288893e9659b73b01bc754ac59bbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784191"
---
# <a name="mediacollectiongetbyalbum-method"></a>Método mediacollection. getByAlbum

O método **GetByAlbum** recupera uma lista de reprodução que contém os itens de mídia do álbum especificado.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = MediaCollection.getByAlbum(
  album
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*álbum* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome do álbum.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um objeto **playlist** .

## <a name="remarks"></a>Comentários

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir usa *mediacollection*. **getByAlbum** para recuperar uma lista de reprodução de itens de mídia. A lista de reprodução contém itens com o álbum especificado pelo usuário em um elemento de entrada de texto HTML chamado getalbum. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!-- Use an HTML BUTTON element to create the playlist and 
then play the digital media items. -->
<INPUT TYPE = "BUTTON"
       NAME = "PlayAlbum" 
       ID = "PlayAlbum"  
       VALUE = "Play Album"

onClick = "
    /* Retrieve the album title text from the user. */
    var album = GetAlbum.value;

    /* Create the playlist using getByAlbum. */
    var pl = Player.mediaCollection.getByAlbum(album);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto mediacollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto playlist**](playlist-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





