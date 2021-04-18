---
description: O método IsDefaultSourceRect determina se o renderizador está usando o retângulo de origem padrão (virtual puro).
ms.assetid: 08c7a365-585c-47e6-9c26-6aa1fa3625e7
title: Método CBaseControlVideo. IsDefaultSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 390ae779eaa7d640d23b40a7e6f6579e158bf6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753365"
---
# <a name="cbasecontrolvideoisdefaultsourcerect-method"></a>Método CBaseControlVideo. IsDefaultSourceRect

O `IsDefaultSourceRect` método determina se o renderizador está usando o retângulo de origem padrão (virtual puro).

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT IsDefaultSourceRect() = 0;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se o renderizador estiver usando a origem padrão; caso contrário, retornará S \_ false.

## <a name="remarks"></a>Comentários

Essa função de membro deve ser implementada na classe derivada. Ele é chamado pela função de membro [**CBaseControlVideo:: IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md) .

O exemplo a seguir demonstra uma implementação dessa função em uma classe derivada.


```C++
// Return S_OK if using the default source; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultSourceRect()
{
    RECT SourceRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetSourceRect(&SourceRect);

    // Check the coordinates that match the video dimensions.

    if (SourceRect.left != 0 || SourceRect.top != 0 ||
            SourceRect.right != pHeader->biWidth ||
                SourceRect.bottom != pHeader->biHeight) {
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

 

 




