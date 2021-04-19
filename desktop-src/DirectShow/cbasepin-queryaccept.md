---
description: 'O método QueryAccept determina se o PIN aceita um tipo de mídia especificado. Esse método implementa o método IPin:: QueryAccept.'
ms.assetid: 7aa25b45-5116-474b-afee-1eddc8b7fd2a
title: Método CBasePin. QueryAccept (Amfilter. h)
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
ms.openlocfilehash: d2c4a982f583d1780dbab37d982fd9a54601e141
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753180"
---
# <a name="cbasepinqueryaccept-method"></a>Método CBasePin. QueryAccept

O `QueryAccept` método determina se o PIN aceita um tipo de mídia especificado. Esse método implementa o método [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QueryAccept(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PMT* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se o tipo de mídia for aceitável. Caso contrário, retornará S \_ false.

## <a name="remarks"></a>Comentários

Na classe base, esse método delega para o método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) . Se **CheckMediaType** falhar, `QueryAccept` retornará S \_ false.

Esse método não mantém a seção crítica do PIN ([**CBasePin:: m \_ pLock**](cbasepin-m-plock.md)). Se a classe derivada modificar dinamicamente o conjunto de tipos de mídia aceitáveis, você deverá substituir esse método para manter a seção crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




