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
ms.openlocfilehash: 28c0c8bcb6efb0e3cbd648c1e45d36e8b18d4b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748639"
---
# <a name="cbaserenderercheckready-method"></a>Método CBaseRenderer. CheckReady

O `CheckReady` método consulta se uma transição de estado foi concluída.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CheckReady();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retornará **true** se a transição de estado estiver concluída ou **false** se o filtro ainda estiver em transição para um novo estado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer:: não é possível ler**](cbaserenderer-notready.md)
</dt> <dt>

[**CBaseRenderer:: pronto**](cbaserenderer-ready.md)
</dt> </dl>

 

 




