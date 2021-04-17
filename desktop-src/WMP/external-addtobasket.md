---
title: Método external. addToBasket
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Método external. addToBasket
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- método addToBasket Windows Media Player
- método addToBasket Windows Media Player, classe externa
- Classe externa Windows Media Player, método addToBasket
topic_type:
- apiref
api_name:
- External.addToBasket
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2fab549dec9e24b0c5bbe61f5511e375c4c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759707"
---
# <a name="externaladdtobasket-method"></a>Método external. addToBasket

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O método **addToBasket** adiciona itens de mídia ao painel de lista (também chamado de cesta) no Windows Media Player.

## <a name="syntax"></a>Sintaxe


```JScript
External.addToBasket(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Modo de exibição* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que especifica o tipo de item que está sendo adicionado ao painel de lista. O chamador deve definir esse parâmetro como uma das seguintes [constantes de localização de biblioteca](library-location-constants.md):

CPListID

CPTrackID

CPAlbumID

CPArtist

CPGenreID

CPAlbumSubGenreID

CPRadioID

</dd> <dt>

*ViewIDs* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém as IDs, delimitada por ponto e vírgula, dos itens a serem adicionados ao painel de lista.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Externalobject para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. basketTitle**](external-baskettitle.md)
</dt> </dl>

 

 





