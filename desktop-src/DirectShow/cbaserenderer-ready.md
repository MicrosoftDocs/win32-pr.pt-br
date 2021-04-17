---
description: O método Ready sinaliza que uma transição de estado foi concluída.
ms.assetid: 01328281-cf25-43fd-9f9c-e55fccbac217
title: Método CBaseRenderer. Ready (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Ready
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a7f70ec258fde7f6208d44c35ca2c284f99e0a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748216"
---
# <a name="cbaserendererready-method"></a>Método CBaseRenderer. Ready

O `Ready` método sinaliza que uma transição de estado foi concluída.

## <a name="syntax"></a>Sintaxe


```C++
void Ready();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método faz com que o método [**CBaseRenderer:: GetState**](cbaserenderer-getstate.md) retorne S \_ OK, o que indica que o filtro concluiu a transição para seu estado atual. O filtro chama esse método sempre que ele conclui uma transição de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::CheckReady**](cbaserenderer-checkready.md)
</dt> <dt>

[**CBaseRenderer:: não é possível ler**](cbaserenderer-notready.md)
</dt> </dl>

 

 




