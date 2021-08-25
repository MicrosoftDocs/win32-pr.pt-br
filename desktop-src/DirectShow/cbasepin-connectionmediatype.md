---
description: O método ConnectionMediaType recupera o tipo de mídia para a conexão de pino atual, se for o caso. Esse método implementa o método IPin::ConnectionMediaType.
ms.assetid: 57d100ba-4171-4caa-ab98-66a0a327a53b
title: Método CBasePin.ConnectionMediaType (Amfilter.h)
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
ms.openlocfilehash: cdeed52a212a659ca280163ea9513f0cb4f373ea2686bfde00078ebccb183daa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916746"
---
# <a name="cbasepinconnectionmediatype-method"></a>Método CBasePin.ConnectionMediaType

O **método ConnectionMediaType** recupera o tipo de mídia para a conexão de pino atual, se for o caso. Esse método implementa o [**método IPin::ConnectionMediaType.**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConnectionMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pgto* 
</dt> <dd>

Ponteiro para uma [**estrutura AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que recebe o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles na tabela a seguir.



| Código de retorno                                                                                           | Descrição                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                   |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>             | Argumento de ponteiro **NULL.**<br/> |
| <dl> <dt>**VFW \_ E \_ NÃO \_ CONECTADO**</dt> </dl> | O pino não está conectado.<br/>      |



 

## <a name="remarks"></a>Comentários

Se o pino estiver conectado, esse método copia o tipo de mídia para a estrutura [**AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) especificada por *pmt*. O chamador deve liberar o bloco de formato do tipo de mídia. Você pode usar a [**função CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ou a função auxiliar [**FreeMediaType.**](freemediatype.md)

Se o pino não estiver conectado, esse método zera o bloco de memória especificado por *pmt* e retornará um código de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

