---
description: O método OnWaitEnd é chamado quando um tempo de espera termina.
ms.assetid: 283627bb-599c-4711-abc4-b5f92dfd29a5
title: Método CBaseVideoRenderer. OnWaitEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36377565556a759c9268ef1bf31ff7774933ccc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748818"
---
# <a name="cbasevideorendereronwaitend-method"></a>Método CBaseVideoRenderer. OnWaitEnd

O método OnWaitEnd é chamado quando um tempo de espera termina.

## <a name="syntax"></a>Sintaxe


```C++
void OnWaitEnd();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função de membro só faz o registro em log de desempenho. Ele é chamado quando o thread está acordado aguardando na janela ou quando o próximo exemplo é devido a ser renderizado. Ele pode, eventualmente, ser usado para reunir informações que controlam a sincronização.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




