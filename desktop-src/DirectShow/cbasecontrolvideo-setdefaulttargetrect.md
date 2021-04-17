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
# <a name="cbasecontrolvideosetdefaulttargetrect-method"></a><span data-ttu-id="cf485-104">Método CBaseControlVideo. SetDefaultTargetRect</span><span class="sxs-lookup"><span data-stu-id="cf485-104">CBaseControlVideo.SetDefaultTargetRect method</span></span>

<span data-ttu-id="cf485-105">O `SetDefaultTargetRect` método define o retângulo de vídeo de destino padrão (virtual puro).</span><span class="sxs-lookup"><span data-stu-id="cf485-105">The `SetDefaultTargetRect` method sets the default target video rectangle (pure virtual).</span></span> <span data-ttu-id="cf485-106">Essa é uma função de membro interna que é chamada quando o retângulo de origem é redefinido.</span><span class="sxs-lookup"><span data-stu-id="cf485-106">This is an internal member function that gets called when the source rectangle is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf485-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf485-107">Syntax</span></span>


```C++
virtual HRESULT SetDefaultTargetRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="cf485-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf485-108">Parameters</span></span>

<span data-ttu-id="cf485-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cf485-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf485-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cf485-110">Return value</span></span>

<span data-ttu-id="cf485-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cf485-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf485-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf485-112">Remarks</span></span>

<span data-ttu-id="cf485-113">Classes derivadas devem substituir isso para redefinir o retângulo de vídeo de destino.</span><span class="sxs-lookup"><span data-stu-id="cf485-113">Derived classes should override this to reset the destination video rectangle.</span></span> <span data-ttu-id="cf485-114">Ele é chamado a partir da função de membro [**CBaseControlVideo:: SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) .</span><span class="sxs-lookup"><span data-stu-id="cf485-114">It is called from the [**CBaseControlVideo::SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) member function.</span></span>

<span data-ttu-id="cf485-115">O exemplo a seguir demonstra uma implementação dessa função em uma classe derivada.</span><span class="sxs-lookup"><span data-stu-id="cf485-115">The following example demonstrates an implementation of this function in a derived class.</span></span>


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



<span data-ttu-id="cf485-116">Neste exemplo, CVideoText é uma classe derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer mantém um objeto de uma classe derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md), e o membro de \_ dados da DrawImage m, definido na classe derivada, mantém um objeto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="cf485-116">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="cf485-117">O \_ membro de dados m mtIn, também definido na classe derivada, mantém um objeto [**CMediaType**](cmediatype.md) com o tipo de mídia do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="cf485-117">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with the media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf485-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf485-118">Requirements</span></span>



| <span data-ttu-id="cf485-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf485-119">Requirement</span></span> | <span data-ttu-id="cf485-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cf485-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf485-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf485-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cf485-122"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf485-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cf485-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cf485-123">Library</span></span><br/> | <dl> <span data-ttu-id="cf485-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="cf485-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf485-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf485-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf485-126">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="cf485-126">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




