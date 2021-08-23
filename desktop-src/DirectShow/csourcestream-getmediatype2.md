---
description: O método GetMediaType recupera um tipo de mídia preferencial.
ms.assetid: 85605885-adb5-4f13-91af-48bf74684eca
title: Método CSourceStream.GetMediaType (Source.h) – parâmetro pMediaType
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
ms.openlocfilehash: 2850d08726337f1ff43ad09319aea8b0af95d107ad9dad9c0f89ce94474c7261
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073190"
---
# <a name="csourcestreamgetmediatype-method-sourceh"></a>Método CSourceStream.GetMediaType (Source.h)

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

Ponteiro para um [**objeto CMediaType**](cmediatype.md) que recebe o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                            | Descrição                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Êxito.<br/>              |
| <dl> <dt>**VFW \_ NÃO TEM MAIS \_ \_ \_ ITENS**</dt> </dl> | Índice fora do intervalo.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Índice menor que zero.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>           | Erro inesperado.<br/>     |



 

## <a name="remarks"></a>Comentários

Há duas versões desse método. Uma versão substitui o [**método CBasePin::GetMediaType**](cbasepin-getmediatype.md) e assume um valor de índice como um parâmetro. A outra versão foi projetada para recuperar um único tipo de mídia, portanto, ela não tem o parâmetro de índice.

O método de parâmetro único retorna E \_ UNEXPECTED. O método de dois parâmetros verifica se o *parâmetro iPosition* é zero e, em seguida, chama a versão de parâmetro único. Dependendo do número de tipos de mídia aos quais o pino dá suporte, você deve substituir um destes métodos:

-   Se o pin dá suporte a exatamente um tipo de mídia, substitua a versão de parâmetro único. Preencha o tipo de mídia ao qual o pino dá suporte.
-   Se o pin for compatível com mais de um tipo de mídia, substitua a versão de dois parâmetros. Substitua também o [**método CSourceStream::CheckMediaType.**](csourcestream-checkmediatype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




