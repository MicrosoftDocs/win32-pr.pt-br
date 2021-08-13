---
title: Media.sourceURL
description: A propriedade sourceURL recupera a URL do item de mídia.
ms.assetid: 98ff6ed4-ad3d-44f8-893d-f016e5217ce5
keywords:
- Media.sourceURL Windows Media Player
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
ms.openlocfilehash: 1e2f99aeb64a73bcf36e2cbd472aedfa8f509a5073e70792e7b47343a1b37d60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415945"
---
# <a name="mediasourceurl"></a>Media.sourceURL

A **propriedade sourceURL** recupera a URL do item de mídia.

## <a name="syntax"></a>Sintaxe

*player*. *currentMedia*.sourceURL

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma Cadeia de Caracteres somente **leitura.**

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *Mídia*. **sourceURL** para recuperar a URL do primeiro item de mídia na playlist de exemplo; a URL do item de mídia é atribuída à propriedade URL do objeto **do** player. O **objeto** Player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> </dl>

 

 





