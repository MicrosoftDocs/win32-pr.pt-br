---
title: Método mediacollection. getByAuthor
description: O método getByAuthor recupera uma lista de reprodução dos itens de mídia pelo autor especificado.
ms.assetid: 8f9b3ee3-a809-4d24-81ce-adad63e5347c
keywords:
- Windows Media Player do método getByAuthor
- método getByAuthor Windows Media Player, classe mediacollection
- classe mediacollection Windows Media Player, método getByAuthor
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
ms.openlocfilehash: 87989d38d49ff87ce26b7394f4ee79ef4bd7197cd0e35dcd5316797df401ba49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574623"
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

o exemplo a seguir JScript usa *mediacollection*. **getByAuthor** para recuperar uma lista de reprodução de itens de mídia. A lista de reprodução contém itens que correspondem ao autor especificado pelo usuário em um elemento de entrada de texto HTML chamado getauthor. O objeto de **jogador** foi criado com ID = "Player".


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

[**Configurações. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





