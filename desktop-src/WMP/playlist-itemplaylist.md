---
title: PLAYLIST. lista de reprodução
description: O atributo doplaylist recupera a lista de reprodução para o item de mídia que é exibido no índice fornecido no elemento PLAYLIST.
ms.assetid: 094bcb5d-8a59-4531-96b8-0e993ca00be6
keywords:
- PLAYLIST. lista de reprodução do Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemPlaylist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d414692050e16dfd0aebe05901bcee0bc26580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782756"
---
# <a name="playlistitemplaylist"></a>PLAYLIST. lista de reprodução

O atributo **Doplaylist** recupera a lista de reprodução para o item de mídia que é exibido no índice fornecido no elemento **playlist** .

``` syntax
        elementID.itemPlaylist(index)
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um objeto de **lista de reprodução** somente leitura.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*index*
</dt> <dd>

**Número**(**longo**) que contém o índice de um item da playlist.

</dd> </dl>

## <a name="remarks"></a>Comentários

A propriedade **Doplaylist** retornará o objeto playlist que é expandido no elemento **playlist** . Por exemplo, se houver duas listas de reprodução aninhadas que não são expandidas no elemento **playlist** e que contiverem três clipes **de mídia cada, a** lista de reprodução (1) retornará a playlist pai que contém as duas listas de reprodução aninhadas. Se a segunda playlist for expandida, a **lista de reprodução (1**) retornará a segunda playlist. Se ambas as listas de reprodução forem expandidas, a lista **de reprodução (** 1) retornará a primeira playlist.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**Objeto playlist**](playlist-object.md)
</dt> </dl>

 

 





