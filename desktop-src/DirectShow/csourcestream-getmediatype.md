---
description: O método GetMediaType recupera um tipo de mídia preferencial. Esse método usa os parâmetros *iPosition* e *pMediaType* .
ms.assetid: c5c5f498-a9a3-4ce7-8cf5-941397aa649d
title: Método CSourceStream. GetMediaType (origem. h)-parâmetros iPosition e pMediaType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb3095e366a03d94616d45eda441fec78d2ccbf7d58f8e74890a42902bae6fc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073250"
---
# <a name="csourcestreamgetmediatype-method-sourceh---iposition-and-pmediatype-parameters"></a>Método CSourceStream. GetMediaType (origem. h)-parâmetros iPosition e pMediaType

O método **GetMediaType** recupera um tipo de mídia preferencial.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iPosition* 
</dt> <dd>

Valor de índice baseado em zero.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que recebe o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                            | Descrição                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Êxito.<br/>              |
| <dl> <dt>**VFW \_ S \_ não há \_ mais \_ itens**</dt> </dl> | Índice fora do intervalo.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Índice menor que zero.<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl>           | Erro inesperado.<br/>     |



 

## <a name="remarks"></a>Comentários

Há duas versões desse método. Uma versão substitui o método [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) e usa um valor de índice como um parâmetro. A outra versão foi projetada para recuperar um único tipo de mídia, portanto, ele não tem o parâmetro de índice.

O método de parâmetro único retorna E \_ inesperado. O método de dois parâmetros verifica se o parâmetro *iPosition* é zero e, em seguida, chama a versão de parâmetro único. Dependendo do número de tipos de mídia aos quais o PIN dá suporte, você deve substituir um destes métodos:

-   Se o PIN der suporte a exatamente um tipo de mídia, substitua a versão de parâmetro único. Preencha o tipo de mídia ao qual o PIN dá suporte.
-   Se o PIN der suporte a mais de um tipo de mídia, substitua a versão de dois parâmetros. Substitua também o método [**CSourceStream:: CheckMediaType**](csourcestream-checkmediatype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro  | Source. h (incluir Fluxos. h)                                                                                    |
| Biblioteca | Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




