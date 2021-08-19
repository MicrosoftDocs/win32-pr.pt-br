---
description: O método IsDefaultTargetRect determina se o renderador está usando o retângulo de destino padrão (virtual puro).
ms.assetid: 60c09515-7a34-421c-b3e8-ce746a935583
title: Método CBaseControlVideo.IsDefaultTargetRect (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c11d5b99610ff88a9e5f4088aa47efdcd8f3d9d676f0b17fad4d8e316324e807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955235"
---
# <a name="cbasecontrolvideoisdefaulttargetrect-method"></a>Método CBaseControlVideo.IsDefaultTargetRect

O `IsDefaultTargetRect` método determina se o renderador está usando o retângulo de destino padrão (virtual puro).

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT IsDefaultTargetRect() = 0;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se o renderdor estiver usando o destino padrão; caso contrário, retornará S \_ FALSE.

## <a name="remarks"></a>Comentários

Essa função membro deve ser implementada na classe derivada. Ele é chamado pela [**função membro CBaseControlVideo::IsUsingDefaultDestination.**](cbasecontrolvideo-isusingdefaultdestination.md)

O exemplo a seguir demonstra uma implementação dessa função em uma classe derivada.


```C++
// Return S_OK if using the default target; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultTargetRect()
{
    RECT TargetRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetTargetRect(&TargetRect);

    // Check the destination that matches the initial client area.

    if (TargetRect.left != 0 || TargetRect.top != 0 ||
            TargetRect.right != m_Size.cx ||
                TargetRect.bottom != m_Size.cy) {
                    return S_FALSE;
    }
    return S_OK;
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

 

 




