---
title: Método Playlist.setItemInfo
description: O método setItemInfo especifica o valor de um atributo de playlist.
ms.assetid: ffecb43f-343d-4a4f-9356-0e3cfa85ce77
keywords:
- Método setItemInfo Windows Media Player
- Método setItemInfo Windows Media Player , classe Playlist
- Classe de playlist Windows Media Player , método setItemInfo
topic_type:
- apiref
api_name:
- Playlist.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47208d1fad03a57e26d1f5591adf658c7553a9087254b49c7aecfd904bd4d95f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335743"
---
# <a name="playlistsetiteminfo-method"></a>Método Playlist.setItemInfo

O **método setItemInfo** especifica o valor de um atributo de playlist.

## <a name="syntax"></a>Sintaxe


```JScript
Playlist.setItemInfo(
  name,
  value
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*name* \[ Em\]
</dt> <dd>

**Cadeia** de caracteres que contém o nome do atributo a ser definido. Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a Referência Windows Media Player [atributo de referência.](attribute-reference.md)

</dd> <dt>

*value* \[ Em\]
</dt> <dd>

**Cadeia** de caracteres que contém o novo valor para o atributo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Um uso especial do **método setItemInfo** é classificar os itens na playlist usando o atributo SortAttribute. O exemplo JScript a seguir classifica uma playlist pelos valores do atributo UserLastPlayedTime. A playlist de variável é uma referência a um **objeto Playlist.**


```JScript
playlist.setItemInfo("SortAttribute", "UserLastPlayedTime")
```



Para usar esse método, é necessário ter acesso completo à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

Consulte a [propriedade attributeCount](playlist-attributecount.md) para ver o código de exemplo que usa essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**Playlist.getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





