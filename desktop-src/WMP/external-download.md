---
title: Método external. download
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método de download inicia o download de um conjunto de itens de mídia.
ms.assetid: 10bae41c-0658-4712-8a7e-375a1ec6dc25
keywords:
- método de download do Windows Media Player
- método de download do Windows Media Player, classe externa
- Classe externa Windows Media Player, método de download
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
ms.openlocfilehash: 35ef0c6e6c32e8959e402080796f29a3860fe728
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789544"
---
# <a name="externaldownload-method"></a>Método external. download

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O método de **Download** inicia o download de um conjunto de itens de mídia.

## <a name="syntax"></a>Sintaxe


```JScript
External.download(
  Type,
  IDs
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tipo* \[ de no\]
</dt> <dd>

Uma [constante de local de biblioteca](library-location-constants.md) que especifica o tipo de item a ser baixado. Por exemplo, CPTrackID especifica que uma ou mais faixas devem ser baixadas.

</dd> <dt>

*IDs* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que contém as IDs, delimitada por ponto e vírgula, dos itens de mídia a serem baixados.

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

[**Baixando conteúdo de mídia**](downloading-media-content.md)
</dt> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Externo. comprar**](external-buy.md)
</dt> <dt>

[**IWMPContentPartner::D aixar**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)
</dt> </dl>

 

 





