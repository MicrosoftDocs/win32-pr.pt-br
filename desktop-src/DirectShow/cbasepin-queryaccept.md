---
description: O método QueryAccept determina se o pino aceita um tipo de mídia especificado. Esse método implementa o método IPin::QueryAccept.
ms.assetid: 7aa25b45-5116-474b-afee-1eddc8b7fd2a
title: Método CBasePin.QueryAccept (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryAccept
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74a179fd1a7f59dcf4e4d22eadf509db9b00cbe482d55e6a6755d7207de8079d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688996"
---
# <a name="cbasepinqueryaccept-method"></a>Método CBasePin.QueryAccept

O `QueryAccept` método determina se o pin aceita um tipo de mídia especificado. Esse método implementa o [**método IPin::QueryAccept.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QueryAccept(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pgto* 
</dt> <dd>

Ponteiro para uma [**estrutura AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se o tipo de mídia for aceitável. Caso contrário, retornará S \_ FALSE.

## <a name="remarks"></a>Comentários

Na classe base, esse método delega ao [**método CBasePin::CheckMediaType.**](cbasepin-checkmediatype.md) Se **CheckMediaType** falhar, `QueryAccept` retornará S \_ FALSE.

Esse método não mantém a seção crítica do pino ([**CBasePin::m \_ pLock**](cbasepin-m-plock.md)). Se a classe derivada modificar dinamicamente o conjunto de tipos de mídia aceitáveis, você deverá substituir esse método para manter a seção crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




