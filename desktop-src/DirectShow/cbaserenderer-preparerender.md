---
description: O método PrepareRender é chamado antes de o filtro renderizar um exemplo.
ms.assetid: 0b137da9-eac0-469f-b457-719a36569c82
title: Método CBaseRenderer. PrepareRender (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee5739a839222900458ae334de6f97fb6d18876b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754547"
---
# <a name="cbaserendererpreparerender-method"></a>Método CBaseRenderer. PrepareRender

O `PrepareRender` método é chamado antes de o filtro renderizar um exemplo.

## <a name="syntax"></a>Sintaxe


```C++
virtual void PrepareRender();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O filtro chama esse método antes de chamar o método [**CBaseRenderer:: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) ou o método [**CBaseRenderer:: render**](cbaserenderer-render.md) . `PrepareRender` Não faz nada na classe base. A classe derivada pode substituí-la para executar as ações necessárias antes da renderização. Por exemplo, um renderizador de vídeo pode substituir esse método para obter sua paleta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




