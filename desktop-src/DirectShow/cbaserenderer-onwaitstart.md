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
ms.openlocfilehash: eaad14d0eec765a0ad12693c0a1eee67386bc9bb26344ee52c29224d129edf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822643"
---
# <a name="cbaserendereronwaitstart-method"></a>Método CBaseRenderer. OnWaitStart

O `OnWaitStart` método é chamado quando o filtro começa a aguardar o tempo de apresentação de um exemplo.

## <a name="syntax"></a>Sintaxe


```C++
virtual void OnWaitStart();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) chama esse método quando ele começa a aguardar o tempo de apresentação de um exemplo. Esse método não faz nada na classe base, mas a classe derivada pode substituí-la.

Se você estiver implementando o controle de qualidade, poderá substituir esse método junto com o método [**CBaseRenderer:: OnWaitEnd**](cbaserenderer-onwaitend.md) . Você pode usar esses métodos para acompanhar o desempenho do filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




