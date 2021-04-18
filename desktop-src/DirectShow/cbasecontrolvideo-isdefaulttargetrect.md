---
description: O método IsDefaultTargetRect determina se o renderizador está usando o retângulo de destino padrão (virtual puro).
ms.assetid: 60c09515-7a34-421c-b3e8-ce746a935583
title: Método CBaseControlVideo. IsDefaultTargetRect (Ctlutil. h)
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
ms.openlocfilehash: e267cc65345d18800beccbc80ac7952c89d781d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749856"
---
# <a name="cbasecontrolvideoisdefaulttargetrect-method"></a>Método CBaseControlVideo. IsDefaultTargetRect

O `IsDefaultTargetRect` método determina se o renderizador está usando o retângulo de destino padrão (virtual puro).

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT IsDefaultTargetRect() = 0;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se o renderizador estiver usando o destino padrão; caso contrário, retornará S \_ false.

## <a name="remarks"></a>Comentários

Essa função de membro deve ser implementada na classe derivada. Ele é chamado pela função de membro [**CBaseControlVideo:: IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md) .

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

 

 




