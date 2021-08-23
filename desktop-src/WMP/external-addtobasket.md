---
title: Método external. addToBasket
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Método external. addToBasket
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- Windows Media Player do método addToBasket
- método addToBasket Windows Media Player, classe externa
- classe externa Windows Media Player, método addToBasket
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
ms.openlocfilehash: 17f51cfc3df641b02a5aa3a0869e810f318357dd70ba67acb3ec2310f8a5a355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650006"
---
# <a name="externaladdtobasket-method"></a>Método external. addToBasket

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O método **addToBasket** adiciona itens de mídia ao painel de lista (também chamado de cesta) em Windows Media Player.

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

## <a name="return-value"></a>Valor retornado

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

 

 





