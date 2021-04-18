---
title: Método mediacollection. getByAuthor
description: O método getByAuthor recupera uma lista de reprodução dos itens de mídia pelo autor especificado.
ms.assetid: 8f9b3ee3-a809-4d24-81ce-adad63e5347c
keywords:
- método getByAuthor Windows Media Player
- método getByAuthor Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método getByAuthor
topic_type:
- apiref
api_name:
- MediaCollection.getByAuthor
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eae0928250e37e76bf3a39f38b43bef8a5691c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810830"
---
# <a name="mediacollectiongetbyauthor-method"></a>Método mediacollection. getByAuthor

O método **getByAuthor** recupera uma lista de reprodução dos itens de mídia pelo autor especificado.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = MediaCollection.getByAuthor(
  author
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*criar* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome do autor.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um objeto **playlist** .

## <a name="remarks"></a>Comentários

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *mediacollection*. **getByAuthor** para recuperar uma lista de reprodução de itens de mídia. A lista de reprodução contém itens que correspondem ao autor especificado pelo usuário em um elemento de entrada de texto HTML chamado getauthor. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play the media items. -->
<INPUT TYPE = "BUTTON"  NAME = "PlayAuthor"  
       ID = "PlayAuthor"  
       VALUE = "Play Author"

onClick = "
    /* Retrieve the author name text from the user. */
    var author = GetAuthor.value;

    /* Create the playlist by using getByAuthor. */
    var pl = Player.mediaCollection.getByAuthor(Author);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media items in the new playlist. */
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

 

 





