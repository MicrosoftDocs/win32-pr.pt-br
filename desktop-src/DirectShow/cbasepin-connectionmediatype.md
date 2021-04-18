---
description: 'O método ConnectionMediaType recupera o tipo de mídia para a conexão do PIN atual, se houver. Esse método implementa o método IPin:: ConnectionMediaType.'
ms.assetid: 57d100ba-4171-4caa-ab98-66a0a327a53b
title: Método CBasePin. ConnectionMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectionMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62bd211b6c93e44c571d822ccc86104a5a6fdcab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771865"
---
# <a name="cbasepinconnectionmediatype-method"></a>Método CBasePin. ConnectionMediaType

O método **ConnectionMediaType** recupera o tipo de mídia para a conexão do PIN atual, se houver. Esse método implementa o método [**IPin:: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConnectionMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PMT* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que recebe o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os da tabela a seguir.



| Código de retorno                                                                                           | Descrição                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                   |
| <dl> <dt>**\_ponteiro E**</dt> </dl>             | Argumento de ponteiro **nulo** .<br/> |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | O PIN não está conectado.<br/>      |



 

## <a name="remarks"></a>Comentários

Se o PIN estiver conectado, esse método copiará o tipo de mídia para a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) especificada por *PGTO*. O chamador deve liberar o bloco de formato do tipo de mídia. Você pode usar a função [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ou a função auxiliar [**FreeMediaType**](freemediatype.md) .

Se o PIN não estiver conectado, esse método zerará o bloco de memória especificado por *PGTO* e retornará um código de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

