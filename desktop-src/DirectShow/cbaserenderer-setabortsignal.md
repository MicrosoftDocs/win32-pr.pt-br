---
description: O método SetAbortSignal define um sinalizador que indica se deve parar a renderização e rejeitar mais exemplos.
ms.assetid: 2dbf3b4d-e285-4d17-a77c-01a16c09d148
title: Método CBaseRenderer. SetAbortSignal (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetAbortSignal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70527d5e43ccab4df7b2110a33df8d813bd16d28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754546"
---
# <a name="cbaserenderersetabortsignal-method"></a>Método CBaseRenderer. SetAbortSignal

O `SetAbortSignal` método define um sinalizador que indica se deve parar a renderização e rejeitar exemplos adicionais.

## <a name="syntax"></a>Sintaxe


```C++
void SetAbortSignal(
   BOOL bAbort
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bAbort* 
</dt> <dd>

Valor booliano que indica se a renderização deve ser interrompida. Se **for true**, o filtro não renderizará mais nenhum exemplo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método define o sinalizador [**CBaseRenderer:: m \_ bAbort**](cbaserenderer-m-babort.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




