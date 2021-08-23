---
title: Método external. compre
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método Buy inicia a compra de um conjunto de itens de mídia.
ms.assetid: 78496de6-214e-4712-8fbc-11e002adce88
keywords:
- Windows Media Player do método de compra
- método de compra Windows Media Player, classe externa
- classe externa Windows Media Player, método de compra
topic_type:
- apiref
api_name:
- External.buy
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16acc578d18c2a93118e1d7aa55b0fdcbe474a8698a0982ef8c2df7edb3802ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649516"
---
# <a name="externalbuy-method"></a>Método external. compre

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O método **Buy** inicia a compra de um conjunto de itens de mídia.

## <a name="syntax"></a>Sintaxe


```JScript
External.buy(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Modo de exibição* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que especifica o tipo de item a ser comprado. O chamador deve definir esse parâmetro como uma das seguintes [constantes de localização de biblioteca](library-location-constants.md):

CPListID

CPTrackID

CPAlbumID

</dd> <dt>

*ViewIDs* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém as IDs, delimitada por ponto e vírgula, dos itens a serem comprados.

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

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Externo. download**](external-download.md)
</dt> <dt>

[**IWMPContentPartner:: comprar**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)
</dt> <dt>

[**Comprando conteúdo de mídia**](purchasing-media-content.md)
</dt> </dl>

 

 





