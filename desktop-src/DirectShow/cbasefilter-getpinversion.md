---
description: O método GetPinVersion recupera um número de versão para o conjunto de Pins neste filtro.
ms.assetid: 6cc186b2-4d9f-4d1c-a8b3-975e9c248df7
title: Método CBaseFilter. GetPinVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a40890ce40e75ebea9f7dd10edb78572eb865ea5f94cd1ec674c082d6df8c631
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640456"
---
# <a name="cbasefiltergetpinversion-method"></a>Método CBaseFilter. GetPinVersion

O `GetPinVersion` método recupera um número de versão para o conjunto de Pins neste filtro.

## <a name="syntax"></a>Sintaxe


```C++
virtual long GetPinVersion();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna a variável de membro [**CBaseFilter:: m \_ PinVersion**](cbasefilter-m-pinversion.md) .

## <a name="remarks"></a>Comentários

O construtor **CBaseFilter** Inicializa a versão do PIN como 1. Na classe base, esse número nunca é alterado. Se o filtro cria ou destrói Pins dinamicamente, ele deve incrementar a versão do PIN sempre que os Pins forem alterados. Para incrementar o número de versão, chame o método [**CBaseFilter:: IncrementPinVersion**](cbasefilter-incrementpinversion.md) .

O objeto enumerador de PIN, que é implementado pela classe [**CEnumPins**](cenumpins.md) , usa a versão do PIN para manter-se sincronizado com o filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




