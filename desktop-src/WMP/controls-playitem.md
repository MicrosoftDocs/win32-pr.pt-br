---
title: Método Controls. playItem
description: O método playItem reproduz o item de mídia especificado. | Método Controls. playItem
ms.assetid: 410e315d-8d5f-4f45-82a7-4249e656c809
keywords:
- método playItem Windows Media Player
- método playItem Windows Media Player, classe Controls
- Classe Controls Windows Media Player, método playItem
topic_type:
- apiref
api_name:
- Controls.playItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9096e378a328f43147a0a94d97034c8e566b611
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783618"
---
# <a name="controlsplayitem-method"></a>Método Controls. playItem

O método **playItem** reproduz o item de mídia especificado.

## <a name="syntax"></a>Sintaxe


```JScript
Controls.playItem(
  theMediaItem
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*theMediaItem* \[ no\]
</dt> <dd>

Objeto de **mídia** a ser reproduzido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O item de mídia será carregado e reproduzido automaticamente, independentemente do valor das *configurações*. Propriedade **AutoStart** . Para carregar um item sem reproduzi-lo automaticamente, defina *configurações*. **AutoStart** para false e atribuir um valor ao *Player*. A **URL**, após a qual a **reprodução** pode ser chamada para iniciar a reprodução do item.

Observação

**playItem** funciona apenas com itens em *currentPlaylist*. Não há suporte para chamar **playItem** com uma referência a um item de mídia salvo.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa **playItem** para reproduzir um item de mídia da playlist atual. O item a ser tocado é escolhido com base na sua posição na lista de reprodução. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
var index = 3

// Retrieve the media item at the fourth position in the current playlist.
var media = Player.currentPlaylist.item(index);

// Play the media item.
Player.controls.playItem(media);

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Lista de reprodução. Item**](playlist-item.md)
</dt> </dl>

 

 





