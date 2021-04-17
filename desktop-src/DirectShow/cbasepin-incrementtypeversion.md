---
description: O método IncrementTypeVersion incrementa o número de versão no conjunto de tipos de mídia preferenciais.
ms.assetid: 30cad0ae-58e7-47f6-94ee-75e24ce0a7e9
title: Método CBasePin. IncrementTypeVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IncrementTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6db3c08972bebbaf1172c44412ae9c8652100da8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748823"
---
# <a name="cbasepinincrementtypeversion-method"></a>Método CBasePin. IncrementTypeVersion

O `IncrementTypeVersion` método incrementa o número de versão no conjunto de tipos de mídia preferenciais.

## <a name="syntax"></a>Sintaxe


```C++
void IncrementTypeVersion();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método incrementa a variável de membro [**CBasePin:: m \_ TypeVersion**](cbasepin-m-typeversion.md) . Se o PIN alterar dinamicamente a lista de tipos de mídia preferenciais, chame esse método sempre que a lista for alterada. Para obter mais informações, consulte [**CBasePin:: GetMediaTypeVersion**](cbasepin-getmediatypeversion.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




