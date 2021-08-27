---
description: O método GetSourceRect recupera o retângulo de origem. Esse é um método interno.
ms.assetid: 51028b79-6aab-4abc-8ee8-2965bda9d191
title: Método CBaseControlVideo.GetSourceRect (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a637e0f5ab5c97494dc072458a29920110363a3e4f07ba8bb7313947996bdad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057046"
---
# <a name="cbasecontrolvideogetsourcerect-method"></a>Método CBaseControlVideo.GetSourceRect

O `GetSourceRect` método recupera o retângulo de origem. Esse é um método interno.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Ponteiro para o retângulo de origem recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

Essa função membro deve ser substituído na classe derivada para retornar o retângulo de origem mantido pelo renderador de vídeo. Ele é chamado das seguintes funções de membro [**CBaseControlVideo.**](cbasecontrolvideo.md)

-   [**CBaseControlVideo::GetSourcePosition**](cbasecontrolvideo-getsourceposition.md)
-   [**CBaseControlVideo::put \_ SourceLeft**](cbasecontrolvideo-put-sourceleft.md)
-   [**CBaseControlVideo::get \_ SourceLeft**](cbasecontrolvideo-get-sourceleft.md)
-   [**CBaseControlVideo::put \_ SourceWidth**](cbasecontrolvideo-put-sourcewidth.md)
-   [**CBaseControlVideo::get \_ SourceWidth**](cbasecontrolvideo-get-sourcewidth.md)
-   [**CBaseControlVideo::put \_ SourceTop**](cbasecontrolvideo-put-sourcetop.md)
-   [**CBaseControlVideo::get \_ SourceTop**](cbasecontrolvideo-get-sourcetop.md)
-   [**CBaseControlVideo::put \_ SourceHeight**](cbasecontrolvideo-put-sourceheight.md)
-   [**CBaseControlVideo::get \_ SourceHeight**](cbasecontrolvideo-get-sourceheight.md)

O exemplo a seguir demonstra uma implementação dessa função em uma classe derivada.


```C++
// Return the current source rectangle
HRESULT CVideoText::GetSourceRect(RECT *pSourceRect)
{
    ASSERT(pSourceRect);
    m_pRenderer->m_DrawImage.GetSourceRect(pSourceRect);
    return NOERROR;
}
```



Neste exemplo, CVideoText é uma classe derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m pRenderer contém um objeto de uma classe derivada de \_ [**CBaseVideoRenderer**](cbasevideorenderer.md)e o membro de dados m DrawImage, definido na classe derivada, contém um objeto \_ [**CDrawImage.**](cdrawimage.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




