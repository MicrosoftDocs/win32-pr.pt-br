---
description: O método OnWaitEnd é chamado quando o filtro é concluído aguardando o tempo de apresentação de um exemplo.
ms.assetid: 47ff8f79-da69-4dcf-8cbb-02c1b56e382e
title: Método CBaseRenderer. OnWaitEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a290ad5d39fc83a4213d1c8a32119b4caa9858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758861"
---
# <a name="cbaserendereronwaitend-method"></a>Método CBaseRenderer. OnWaitEnd

O `OnWaitEnd` método é chamado quando o filtro é concluído aguardando o tempo de apresentação de um exemplo.

## <a name="syntax"></a>Sintaxe


```C++
virtual void OnWaitEnd();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) chama esse método quando ele termina de aguardar o tempo de apresentação de um exemplo. Esse método não faz nada na classe base, mas a classe derivada pode substituí-la.

Se você estiver implementando o controle de qualidade, poderá substituir esse método junto com o método [**CBaseRenderer:: OnWaitStart**](cbaserenderer-onwaitstart.md) . Você pode usar esses métodos para acompanhar o desempenho do filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




