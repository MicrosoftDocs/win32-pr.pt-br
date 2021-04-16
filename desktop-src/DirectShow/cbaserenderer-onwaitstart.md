---
description: O método OnWaitStart é chamado quando o filtro começa a aguardar o tempo de apresentação de um exemplo.
ms.assetid: 598cd676-3afe-4ec9-ae38-83971412e6a7
title: Método CBaseRenderer. OnWaitStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2f88f11e370c6d1962ae6076f4c8f5eecc31407
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757432"
---
# <a name="cbaserendereronwaitstart-method"></a>Método CBaseRenderer. OnWaitStart

O `OnWaitStart` método é chamado quando o filtro começa a aguardar o tempo de apresentação de um exemplo.

## <a name="syntax"></a>Sintaxe


```C++
virtual void OnWaitStart();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) chama esse método quando ele começa a aguardar o tempo de apresentação de um exemplo. Esse método não faz nada na classe base, mas a classe derivada pode substituí-la.

Se você estiver implementando o controle de qualidade, poderá substituir esse método junto com o método [**CBaseRenderer:: OnWaitEnd**](cbaserenderer-onwaitend.md) . Você pode usar esses métodos para acompanhar o desempenho do filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




