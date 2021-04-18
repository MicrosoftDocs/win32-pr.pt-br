---
description: 'O método CheckMediaType determina se o PIN aceita um tipo de mídia específico. Esse método implementa o método puramente virtual CBasePin:: CheckMediaType.'
ms.assetid: 3db7c74c-a6aa-4b49-b2a5-9bf8db35fd7e
title: Método CSourceStream. CheckMediaType (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f8b6c18613f5c187fc637febd08b74260a1e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751681"
---
# <a name="csourcestreamcheckmediatype-method"></a>Método CSourceStream. CheckMediaType

O `CheckMediaType` método determina se o PIN aceita um tipo de mídia específico. Esse método implementa o método puramente virtual [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) .

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaType* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que contém o tipo de mídia proposto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                            | Descrição                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Este PIN dá suporte a este tipo de mídia.<br/>        |
| <dl> <dt>**E \_ falha**</dt> </dl> | O PIN não oferece suporte a esse tipo de mídia.<br/> |



 

## <a name="remarks"></a>Comentários

Por padrão, o PIN dá suporte a um único tipo de mídia. Esse método recupera o tipo com suporte chamando a versão de parâmetro único do método [**CSourceStream:: GetMediaType**](csourcestream-getmediatype.md) e o compara com o tipo proposto. Se o PIN der suporte a mais de um tipo de mídia, substitua esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




