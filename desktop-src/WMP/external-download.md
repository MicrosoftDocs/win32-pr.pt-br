---
title: Método External.download
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método de download inicia o download de um conjunto de itens de mídia.
ms.assetid: 10bae41c-0658-4712-8a7e-375a1ec6dc25
keywords:
- download do método Windows Media Player
- baixar método Windows Media Player , classe externa
- Classe externa Windows Media Player , método de download
topic_type:
- apiref
api_name:
- External.download
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 766f96a6db5f2114724e7545eaac7a269bf52e2e657872a8078b490621c794df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649216"
---
# <a name="externaldownload-method"></a>Método External.download

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O **método** de download inicia o download de um conjunto de itens de mídia.

## <a name="syntax"></a>Sintaxe


```JScript
External.download(
  Type,
  IDs
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tipo* \[ Em\]
</dt> <dd>

Uma [constante de local da](library-location-constants.md) biblioteca que especifica o tipo de item a ser baixado. Por exemplo, CPTrackID especifica que uma ou mais faixas devem ser baixadas.

</dd> <dt>

*IDs* \[ Em\]
</dt> <dd>

**Cadeia** de caracteres que contém as IDs, delimitadas por ponto e vírgula, dos itens de mídia a serem baixados.

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

[**Baixando conteúdo de mídia**](downloading-media-content.md)
</dt> <dt>

[**Objeto externo para lojas online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.buy**](external-buy.md)
</dt> <dt>

[**IWMPContentPartner::D ownload**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)
</dt> </dl>

 

 





