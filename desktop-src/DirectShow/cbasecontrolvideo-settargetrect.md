---
description: O método SetTargetRect define o retângulo de destino atual (virtual puro). Essa é uma função de membro interna que é chamada quando o retângulo de destino é alterado.
ms.assetid: 9e48989d-5995-4f9d-82b2-01229473c3e8
title: Método CBaseControlVideo. SetTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3868e7d8df93940829fb96c7152a55048a5cae82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755622"
---
# <a name="cbasecontrolvideosettargetrect-method"></a>Método CBaseControlVideo. SetTargetRect

O `SetTargetRect` método define o retângulo de destino atual (virtual puro). Essa é uma função de membro interna que é chamada quando o retângulo de destino é alterado.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT SetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Ponteiro para o retângulo de destino.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Classes derivadas devem substituir isso para saber quando o retângulo de destino é alterado. Ele é chamado a partir das seguintes funções de membro.

-   [**CBaseControlVideo::SetDestinationPosition**](cbasecontrolvideo-setdestinationposition.md)
-   [**CBaseControlVideo::p UT \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)
-   [**CBaseControlVideo::p UT \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)
-   [**CBaseControlVideo::p UT \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)
-   [**CBaseControlVideo::p UT \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)

O exemplo a seguir demonstra uma implementação dessa função em uma classe derivada.


```C++
HRESULT CVideoText::SetTargetRect(RECT *pTargetRect)
{
    m_pRenderer->m_DrawImage.SetTargetRect(pTargetRect);
    return NOERROR;
}
```



Neste exemplo, CVideoText é uma classe derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer mantém um objeto de uma classe derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md), e o membro de \_ dados da DrawImage m, definido na classe derivada, mantém um objeto [**CDrawImage**](cdrawimage.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




