---
title: Método playlist. getItemInfo
description: O método getItemInfo recupera o valor de um atributo de playlist.
ms.assetid: 888c0ab7-c225-4246-b1a1-94da7e19fa1a
keywords:
- método getItemInfo Windows Media Player
- método getItemInfo Windows Media Player, classe playlist
- Classe playlist Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- Playlist.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b1151528d6cf4e36aaed1cb4dc48a70f4083c4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751511"
---
# <a name="playlistgetiteminfo-method"></a>Método playlist. getItemInfo

O método **getItemInfo** recupera o valor de um atributo de playlist.

## <a name="syntax"></a>Sintaxe


```JScript
strRetVal = Playlist.getItemInfo(
  name
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome do atributo a ser recuperado. Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna uma **cadeia de caracteres**.

## <a name="remarks"></a>Comentários

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

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

[**Playlist. setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





