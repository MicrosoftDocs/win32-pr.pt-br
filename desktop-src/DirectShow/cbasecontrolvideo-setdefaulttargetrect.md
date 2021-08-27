---
description: O método SetDefaultTargetRect define o retângulo de vídeo de destino padrão (virtual puro). Essa é uma função membro interna que é chamada quando o retângulo de origem é redefinido.
ms.assetid: bb7e32b2-f02c-465f-a8cb-6172d9724790
title: Método CBaseControlVideo.SetDefaultTargetRect (Ctlutil.h)
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
ms.openlocfilehash: 1ab9cf310ffc35df07ecd9e332325bb5f20f3cb4884ee17e672294b89c5abc9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087476"
---
# <a name="cbasecontrolvideosetdefaulttargetrect-method"></a>Método CBaseControlVideo.SetDefaultTargetRect

O `SetDefaultTargetRect` método define o retângulo de vídeo de destino padrão (virtual puro). Essa é uma função membro interna que é chamada quando o retângulo de origem é redefinido.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT SetDefaultTargetRect() = 0;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

As classes derivadas devem substituir isso para redefinir o retângulo de vídeo de destino. Ele é chamado da [**função membro CBaseControlVideo::SetDefaultDestinationPosition.**](cbasecontrolvideo-setdefaultdestinationposition.md)

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



Neste exemplo, CVideoText é uma classe derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m pRenderer contém um objeto de uma classe derivada de \_ [**CBaseVideoRenderer**](cbasevideorenderer.md)e o membro de dados m DrawImage, definido na classe derivada, contém um objeto \_ [**CDrawImage.**](cdrawimage.md) O membro de dados mtIn, também definido na classe derivada, contém um \_ [**objeto CMediaType**](cmediatype.md) com o tipo de mídia do pino de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




