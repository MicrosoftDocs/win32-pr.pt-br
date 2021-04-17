---
title: Media. sourceURL
description: A propriedade sourceURL recupera a URL do item de mídia.
ms.assetid: 98ff6ed4-ad3d-44f8-893d-f016e5217ce5
keywords:
- Media. sourceURL Windows Media Player
topic_type:
- apiref
api_name:
- Media.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c32d594cd1c3b590001eedfd09e9a8c8eb21240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783739"
---
# <a name="mediasourceurl"></a>Media. sourceURL

A propriedade **sourceURL** recupera a URL do item de mídia.

## <a name="syntax"></a>Syntax

*Player*. *currentMedia*. sourceURL

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** somente leitura.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *mídia*. **sourceURL** para recuperar a URL do primeiro item de mídia na playlist de exemplo; a URL do item de mídia é atribuída à propriedade **URL** do objeto Player. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Store the sample playlist object in a variable. 
var pl = Player.playlistCollection.getByName("Sample Playlist").item(0);

// Store the first media item from the sample playlist.
var media = pl.item(0);

// Change the URL property of the player to the URL of the media item.
Player.URL = media.sourceURL;

// Play the media item.
Player.controls.play();

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> </dl>

 

 





