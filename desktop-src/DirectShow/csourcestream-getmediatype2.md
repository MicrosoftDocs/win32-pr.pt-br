---
description: O método GetMediaType recupera um tipo de mídia preferencial.
ms.assetid: 85605885-adb5-4f13-91af-48bf74684eca
title: Método CSourceStream. GetMediaType (origem. h)
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
ms.openlocfilehash: c62d79faab8d48d748f4a2c787dd1cbc8f6d2ed7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758849"
---
# <a name="csourcestreamgetmediatype-method-sourceh"></a>Método CSourceStream. GetMediaType (origem. h)

O `GetMediaType` método recupera um tipo de mídia preferencial.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaType* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que recebe o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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
| parâmetro<br/>  | <dl> <dt>Source. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




