---
title: Método mediacollection. getByName
description: O método getByName recupera uma lista de reprodução dos itens de mídia com o nome especificado.
ms.assetid: f9395a4f-06d6-438b-b7c5-7a063abdf59f
keywords:
- método getByName Windows Media Player
- método getByName Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método getByName
topic_type:
- apiref
api_name:
- MediaCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01a3fc6e34b508fa094f79d2fbbd1d44ab712789
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758191"
---
# <a name="mediacollectiongetbyname-method"></a>Método mediacollection. getByName

O método **getByName** recupera uma lista de reprodução dos itens de mídia com o nome especificado.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = MediaCollection.getByName(
  name
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um objeto **playlist** .

## <a name="remarks"></a>Comentários

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *mediacollection*. **getByName** para recuperar três itens da biblioteca. Cada item é acrescentado à playlist atual. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// In each case, use the name exactly as it appears in the library.
// Windows Media Player does not include file name extensions or file paths
// in the name. Internet URLs include the entire path, but not the 
// file name extension.

// Get a playlist object that contains an Internet URL.
var One = Player.mediaCollection.getByName("https://www.proseware.com/Media/Laure");
 
// Get a playlist object that contains a file on a network server.
var Two = Player.mediaCollection.getByName("Jeanne");

// Get a playlist object that contains a file on a local drive.
var Three = Player.mediaCollection.getByName("house");

// Append each item to the current playlist. Since each playlist retrieved
// using getByName contains one digital media item, use Playlist.item with
// an index of zero to reference that item.
Player.currentPlaylist.appendItem(One.item(0));
Player.currentPlaylist.appendItem(Two.item(0));
Player.currentPlaylist.appendItem(Three.item(0));

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

 

 





