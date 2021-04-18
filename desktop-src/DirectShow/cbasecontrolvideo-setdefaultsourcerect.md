---
description: O método SetDefaultSourceRect define o retângulo de vídeo de origem padrão (virtual puro). Isso em uma função membro interna que é chamada quando o retângulo de origem é redefinido.
ms.assetid: d0dae0a9-8763-485e-b9d3-80076a3f2f35
title: Método CBaseControlVideo. SetDefaultSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82fe2001a42ca75fff4f3172c8ce05da18881d73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771875"
---
# <a name="cbasecontrolvideosetdefaultsourcerect-method"></a><span data-ttu-id="c7b23-104">Método CBaseControlVideo. SetDefaultSourceRect</span><span class="sxs-lookup"><span data-stu-id="c7b23-104">CBaseControlVideo.SetDefaultSourceRect method</span></span>

<span data-ttu-id="c7b23-105">O `SetDefaultSourceRect` método define o retângulo de vídeo de origem padrão (virtual puro).</span><span class="sxs-lookup"><span data-stu-id="c7b23-105">The `SetDefaultSourceRect` method sets the default source video rectangle (pure virtual).</span></span> <span data-ttu-id="c7b23-106">Isso em uma função membro interna que é chamada quando o retângulo de origem é redefinido.</span><span class="sxs-lookup"><span data-stu-id="c7b23-106">This in an internal member function that gets called when the source rectangle is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7b23-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7b23-107">Syntax</span></span>


```C++
virtual HRESULT SetDefaultSourceRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="c7b23-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7b23-108">Parameters</span></span>

<span data-ttu-id="c7b23-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c7b23-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7b23-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7b23-110">Return value</span></span>

<span data-ttu-id="c7b23-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c7b23-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7b23-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7b23-112">Remarks</span></span>

<span data-ttu-id="c7b23-113">Classes derivadas devem substituir isso para redefinir o retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="c7b23-113">Derived classes should override this to reset the source rectangle.</span></span> <span data-ttu-id="c7b23-114">Ele é chamado de [**CBaseControlVideo:: SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md).</span><span class="sxs-lookup"><span data-stu-id="c7b23-114">It is called from [**CBaseControlVideo::SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md).</span></span>

<span data-ttu-id="c7b23-115">O exemplo a seguir demonstra uma implementação dessa função em uma classe derivada.</span><span class="sxs-lookup"><span data-stu-id="c7b23-115">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// This is called when you reset the default source rectangle.
HRESULT CVideoText::SetDefaultSourceRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT SourceRect = {0,0,pHeader->biWidth,pHeader->biHeight};
    m_pRenderer->m_DrawImage.SetSourceRect(&SourceRect);
    return NOERROR;
}
```



<span data-ttu-id="c7b23-116">Neste exemplo, CVideoText é uma classe derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer mantém um objeto de uma classe derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md), e o membro de \_ dados da DrawImage m, definido na classe derivada, mantém um objeto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="c7b23-116">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="c7b23-117">O \_ membro de dados m mtIn, também definido na classe derivada, mantém um objeto [**CMediaType**](cmediatype.md) com o tipo de mídia do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="c7b23-117">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7b23-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7b23-118">Requirements</span></span>



| <span data-ttu-id="c7b23-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7b23-119">Requirement</span></span> | <span data-ttu-id="c7b23-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c7b23-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7b23-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7b23-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c7b23-122"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7b23-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c7b23-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7b23-123">Library</span></span><br/> | <dl> <span data-ttu-id="c7b23-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c7b23-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7b23-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7b23-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7b23-126">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="c7b23-126">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




