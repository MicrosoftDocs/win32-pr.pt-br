---
title: Método MediaCollection.getByName
description: O método getByName recupera uma playlist dos itens de mídia com o nome especificado.
ms.assetid: f9395a4f-06d6-438b-b7c5-7a063abdf59f
keywords:
- Método getByName Windows Media Player
- Método getByName Windows Media Player classe , MediaCollection
- Classe MediaCollection Windows Media Player método , getByName
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
ms.openlocfilehash: 15063a9d544f6ebe55e66513b79aeead7c94e8aeffed7571ccb2ac574e1cb876
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996286"
---
# <a name="mediacollectiongetbyname-method"></a>Método MediaCollection.getByName

O **método getByName** recupera uma playlist dos itens de mídia com o nome especificado.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = MediaCollection.getByName(
  name
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*name* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que contém o nome.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **objeto Playlist.**

## <a name="remarks"></a>Comentários

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir *usa MediaCollection*. **getByName** para recuperar três itens da biblioteca. Cada item é então anexado à playlist atual. O **objeto** Player foi criado com ID="Player".


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

 

 





