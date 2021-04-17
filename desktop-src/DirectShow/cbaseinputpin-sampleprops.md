---
description: O método SampleProps recupera as propriedades da amostra mais recente, em uma estrutura de \_ Propriedades am SAMPLE2 \_ .
ms.assetid: d4c98c35-f8b2-4111-bae9-4e0f58a0cc8a
title: Método CBaseInputPin. SampleProps (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.SampleProps
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45663cfd221c7a31abe5f85a494869b24d1ddd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752908"
---
# <a name="cbaseinputpinsampleprops-method"></a>Método CBaseInputPin. SampleProps

O `SampleProps` método recupera as propriedades da amostra mais recente, em uma estrutura [**de \_ \_ Propriedades SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

## <a name="syntax"></a>Sintaxe


```C++
AM_SAMPLE2_PROPERTIES* SampleProps();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna o endereço da variável de membro [**CBaseInputPin:: m \_ SampleProps**](cbaseinputpin-m-sampleprops.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




