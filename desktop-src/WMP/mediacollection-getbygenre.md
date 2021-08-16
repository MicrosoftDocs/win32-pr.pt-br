---
title: Método MediaCollection.getByGenre
description: O método getByGenre recupera uma playlist dos itens de mídia com o gênero especificado.
ms.assetid: 022a0c52-93e1-4ab4-90a7-632bcd6fc004
keywords:
- Método getByGenre Windows Media Player
- Método getByGenre Windows Media Player classe , MediaCollection
- Classe MediaCollection Windows Media Player método , getByGenre
topic_type:
- apiref
api_name:
- MediaCollection.getByGenre
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06df514e7ed399e73f6778912df32a4ed0be57a90039fe867c75cf31a3eec807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135009"
---
# <a name="mediacollectiongetbygenre-method"></a>Método MediaCollection.getByGenre

O **método getByGenre** recupera uma playlist dos itens de mídia com o gênero especificado.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = MediaCollection.getByGenre(
  genre
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*gênero* \[ Em\]
</dt> <dd>

**Cadeia** de caracteres que contém o nome do gênero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **objeto Playlist.**

## <a name="remarks"></a>Comentários

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir *usa MediaCollection*. **getByGenre para** recuperar uma playlist de itens de mídia. A playlist contém itens com o gênero especificado pelo usuário em um elemento de entrada HTML TEXT chamado GetGenre. O **objeto** Player foi criado com ID = "Player".


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play 
the media items. -->
<INPUT TYPE = "BUTTON"  
       NAME = "PlayGenre"  
       ID = "PlayGenre"  
       VALUE = "Play Genre"

onClick = "
    /* Retrieve the genre text from the user. */
    var genre = GetGenre.value;

    /* Create the playlist using getByGenre. */
    var pl = Player.mediaCollection.getByGenre(genre);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the digital media item in the new playlist. */
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

 

 





