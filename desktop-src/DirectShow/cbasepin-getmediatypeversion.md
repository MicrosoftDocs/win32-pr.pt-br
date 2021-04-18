---
description: O método GetMediaTypeVersion recupera um número de versão para o conjunto de tipos de mídia preferenciais.
ms.assetid: bd7b8070-eac5-458c-ada0-7fb0d789dd54
title: Método CBasePin. GetMediaTypeVersion (Amfilter. h)
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
ms.openlocfilehash: fe01d33d7a7c1cb65bc0e2391af63e3519d9cce3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749031"
---
# <a name="cbasepingetmediatypeversion-method"></a>Método CBasePin. GetMediaTypeVersion

O `GetMediaTypeVersion` método recupera um número de versão para o conjunto de tipos de mídia preferenciais.

## <a name="syntax"></a>Sintaxe


```C++
virtual LONG GetMediaTypeVersion();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna a variável de membro [**CBasePin:: m \_ TypeVersion**](cbasepin-m-typeversion.md) .

## <a name="remarks"></a>Comentários

O construtor **CBasePin** Inicializa o número de versão para 1. Na classe base, esse número nunca é alterado. Se o PIN alterar dinamicamente sua lista de tipos de mídia preferenciais, ele deverá incrementar o número de versão sempre que a lista for alterada. Para incrementar o número de versão, chame o método [**CBasePin:: IncrementTypeVersion**](cbasepin-incrementtypeversion.md) .

O enumerador de tipo de mídia, que é implementado pela classe [**CEnumMediaTypes**](cenummediatypes.md) , usa o número de versão para manter-se sincronizado com o PIN.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




