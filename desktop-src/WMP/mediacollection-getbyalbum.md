---
title: Método MediaCollection.getByAlbum
description: O método GetByAlbum recupera uma playlist que contém os itens de mídia do álbum especificado.
ms.assetid: e7e72f0e-e0ae-4bbd-a8b7-966f0fc50059
keywords:
- Método getByAlbum Windows Media Player
- Método getByAlbum Windows Media Player classe , MediaCollection
- Classe MediaCollection Windows Media Player método , getByAlbum
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
ms.openlocfilehash: 7c17b7113b66f49822bad5586033312c9ec50711e6290c3f655a0a1b75adc54c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574669"
---
# <a name="mediacollectiongetbyalbum-method"></a>Método MediaCollection.getByAlbum

O **método GetByAlbum** recupera uma playlist que contém os itens de mídia do álbum especificado.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = MediaCollection.getByAlbum(
  album
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*álbum* \[ Em\]
</dt> <dd>

**Cadeia** de caracteres que contém o nome do álbum.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um **objeto Playlist.**

## <a name="remarks"></a>Comentários

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="examples"></a>Exemplos

O exemplo a seguir usa *MediaCollection*. **getByAlbum para** recuperar uma playlist de itens de mídia. A playlist contém itens com o álbum especificado pelo usuário em um elemento de entrada HTML TEXT chamado GetAlbum. O **objeto** Player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





