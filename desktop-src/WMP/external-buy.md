---
title: Método external. compre
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método Buy inicia a compra de um conjunto de itens de mídia.
ms.assetid: 78496de6-214e-4712-8fbc-11e002adce88
keywords:
- método de compra Windows Media Player
- método de compra Windows Media Player, classe externa
- Classe externa Windows Media Player, método de compra
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
ms.openlocfilehash: a5ffee188372e33ed4ceadf1bb1ee2ea0f986207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762072"
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

## <a name="return-value"></a>Retornar valor

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

 

 





