---
description: O método OnRenderStart é chamado quando a renderização está prestes a ser iniciada.
ms.assetid: 46af24cf-9075-4ebc-a49b-85f8f0c3da6f
title: Método CBaseRenderer. OnRenderStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7838b0ba43c1e570b745541882a2f2f815dd948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783193"
---
# <a name="cbaserendereronrenderstart-method"></a>Método CBaseRenderer. OnRenderStart

O `OnRenderStart` método é chamado quando a renderização está prestes a ser iniciada.

## <a name="syntax"></a>Sintaxe


```C++
virtual void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método [**CBaseRenderer:: render**](cbaserenderer-render.md) chama esse método. Ele não faz nada na classe base, mas a classe derivada pode substituí-la; por exemplo, para coletar dados de controle de qualidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




