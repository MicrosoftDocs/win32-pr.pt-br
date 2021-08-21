---
description: O método EndFlush encerra uma operação de liberação. Esse método substitui o método CTransformFilter::EndFlush.
ms.assetid: e7dfc6f9-1630-426b-95b2-9814331b5e61
title: Método CVideoTransformFilter.EndFlush (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 359229e690715667d7bbfbe3d3a9134f41f5af9febc185885e08cde7d986896e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155870"
---
# <a name="cvideotransformfilterendflush-method"></a>Método CVideoTransformFilter.EndFlush

O `EndFlush` método encerra uma operação de liberação. Esse método substitui o [**método CTransformFilter::EndFlush.**](ctransformfilter-endflush.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se for bem-sucedido ou um código de erro.

## <a name="remarks"></a>Comentários

Esse método redefine todas as medidas de desempenho internas do filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Vtrans.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




