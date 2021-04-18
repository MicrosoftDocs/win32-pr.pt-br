---
title: Método playlist. setItemInfo
description: O método setItemInfo especifica o valor de um atributo de playlist.
ms.assetid: ffecb43f-343d-4a4f-9356-0e3cfa85ce77
keywords:
- método setItemInfo Windows Media Player
- método setItemInfo Windows Media Player, classe playlist
- Classe playlist Windows Media Player, método setItemInfo
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
ms.openlocfilehash: 8ff42e56e549100044db0881bb38ade5f2f1711a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813658"
---
# <a name="playlistsetiteminfo-method"></a>Método playlist. setItemInfo

O método **setItemInfo** especifica o valor de um atributo de playlist.

## <a name="syntax"></a>Sintaxe


```JScript
Playlist.setItemInfo(
  name,
  value
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome do atributo a ser definido. Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.

</dd> <dt>

*valor* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que contém o novo valor para o atributo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Um uso especial do método **setItemInfo** é classificar os itens na lista de reprodução usando o atributo SortAttribute. O exemplo de JScript a seguir classifica uma lista de reprodução pelos valores do atributo UserLastPlayedTime. A playlist de variável é uma referência a um objeto de **playlist** .


```JScript
playlist.setItemInfo("SortAttribute", "UserLastPlayedTime")
```



Para usar esse método, é necessário ter acesso completo à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

Consulte a propriedade [attributeCount](playlist-attributecount.md) para obter o código de exemplo que usa essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto playlist**](playlist-object.md)
</dt> <dt>

[**Playlist. getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





