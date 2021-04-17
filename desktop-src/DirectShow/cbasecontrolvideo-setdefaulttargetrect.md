---
description: O método SetDefaultTargetRect define o retângulo de vídeo de destino padrão (virtual puro). Essa é uma função de membro interna que é chamada quando o retângulo de origem é redefinido.
ms.assetid: bb7e32b2-f02c-465f-a8cb-6172d9724790
title: Método CBaseControlVideo. SetDefaultTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54b31268935cb296543b3992bf67b7a2193c1a92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748837"
---
# <a name="cbasecontrolvideosetdefaulttargetrect-method"></a>Método CBaseControlVideo. SetDefaultTargetRect

O `SetDefaultTargetRect` método define o retângulo de vídeo de destino padrão (virtual puro). Essa é uma função de membro interna que é chamada quando o retângulo de origem é redefinido.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT SetDefaultTargetRect() = 0;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Classes derivadas devem substituir isso para redefinir o retângulo de vídeo de destino. Ele é chamado a partir da função de membro [**CBaseControlVideo:: SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) .

O exemplo a seguir demonstra uma implementação dessa função em uma classe derivada.


```C++
// This is called when you reset the default target rectangle.
HRESULT CVideoText::SetDefaultTargetRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT TargetRect = {0,0,m_Size.cx,m_Size.cy};
    m_pRenderer->m_DrawImage.SetTargetRect(&TargetRect);
    return NOERROR;
}
```



Neste exemplo, CVideoText é uma classe derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer mantém um objeto de uma classe derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md), e o membro de \_ dados da DrawImage m, definido na classe derivada, mantém um objeto [**CDrawImage**](cdrawimage.md) . O \_ membro de dados m mtIn, também definido na classe derivada, mantém um objeto [**CMediaType**](cmediatype.md) com o tipo de mídia do pino de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




