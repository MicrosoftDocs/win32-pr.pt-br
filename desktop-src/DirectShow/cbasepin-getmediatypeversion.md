---
description: O método GetMediaTypeVersion recupera um número de versão para o conjunto de tipos de mídia preferenciais.
ms.assetid: bd7b8070-eac5-458c-ada0-7fb0d789dd54
title: Método CBasePin.GetMediaTypeVersion (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f1b50b16a099c8698bbf5bef270173334f1c3ac2c3d2d67ff87778cffddf2ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955185"
---
# <a name="cbasepingetmediatypeversion-method"></a>Método CBasePin.GetMediaTypeVersion

O `GetMediaTypeVersion` método recupera um número de versão para o conjunto de tipos de mídia preferenciais.

## <a name="syntax"></a>Sintaxe


```C++
virtual LONG GetMediaTypeVersion();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna a [**variável de membro \_ TypeVersion CBasePin::m.**](cbasepin-m-typeversion.md)

## <a name="remarks"></a>Comentários

O **construtor CBasePin** inicializa o número de versão como 1. Na classe base, esse número nunca muda. Se o pin mudar dinamicamente sua lista de tipos de mídia preferenciais, ele deverá incrementar o número de versão sempre que a lista for modificada. Para incrementar o número de versão, chame o [**método CBasePin::IncrementTypeVersion.**](cbasepin-incrementtypeversion.md)

O enumerador de tipo de mídia, que é implementado pela [**classe CEnumMediaTypes,**](cenummediatypes.md) usa o número de versão para se manter sincronizado com o pino.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




