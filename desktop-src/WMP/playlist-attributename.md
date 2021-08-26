---
title: Playlist. attributeName
description: A propriedade attributeName recupera o nome de um atributo em um índice especificado.
ms.assetid: 3ff68e78-5fa1-4ca6-aa59-4752dbaee52a
keywords:
- Windows Media Player de playlist. attributeName
topic_type:
- apiref
api_name:
- Playlist.attributeName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 695e0ee00aca0fe7743a028e0e7830e1839c0b2f89b42a94e9ce1dbe29ef35ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003206"
---
# <a name="playlistattributename"></a>Playlist. attributeName

A propriedade **AttributeName** recupera o nome de um atributo em um índice especificado.

## <a name="syntax"></a>Syntax

*Player*. *currentPlaylist*. **AttributeName**( *índice* )

## <a name="parameters"></a>Parâmetros

*index*

**Número** (**longo**) que contém o índice.

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** somente leitura.

## <a name="remarks"></a>Comentários

O número de atributos é recuperado pela propriedade **attributeCount** . Dado um índice, **AttributeName** retorna uma **cadeia de caracteres** que pode ser usada em conjunto com **setItemInfo** ou **getItemInfo** para especificar ou recuperar um valor para o atributo.

Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

para obter informações sobre os atributos com suporte pelo Windows Media Player, consulte a [referência de atributo](attribute-reference.md)Windows Media Player.

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

[**Playlist. attributeCount**](playlist-attributecount.md)
</dt> <dt>

[**Playlist. getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Playlist. setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Configurações. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





