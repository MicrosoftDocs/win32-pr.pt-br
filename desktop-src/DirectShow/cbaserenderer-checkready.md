---
description: O método CheckReady consulta se uma transição de estado foi concluída.
ms.assetid: dfa669ed-a5ab-498e-9fc2-ff15d6ddbc13
title: Método CBaseRenderer. CheckReady (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a1fac55eba92141ac8174b30ed2dcbc4685ba250b7bb21236432bb998b3b5e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043946"
---
# <a name="cbaserenderercheckready-method"></a>Método CBaseRenderer. CheckReady

O `CheckReady` método consulta se uma transição de estado foi concluída.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CheckReady();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará **true** se a transição de estado estiver concluída ou **false** se o filtro ainda estiver em transição para um novo estado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer:: não é possível ler**](cbaserenderer-notready.md)
</dt> <dt>

[**CBaseRenderer:: pronto**](cbaserenderer-ready.md)
</dt> </dl>

 

 




