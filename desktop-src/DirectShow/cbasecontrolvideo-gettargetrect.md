---
description: O método GetTargetRect recupera o retângulo de destino. Essa é uma função membro auxiliar interna.
ms.assetid: bf9d95c9-eee8-46b8-bdee-a7d16777ed83
title: Método CBaseControlVideo. GetTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d59a12e134edf37c8ab0a63f46f77923b112605d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769251"
---
# <a name="cbasecontrolvideogettargetrect-method"></a><span data-ttu-id="6099b-104">Método CBaseControlVideo. GetTargetRect</span><span class="sxs-lookup"><span data-stu-id="6099b-104">CBaseControlVideo.GetTargetRect method</span></span>

<span data-ttu-id="6099b-105">O `GetTargetRect` método recupera o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="6099b-105">The `GetTargetRect` method retrieves the destination rectangle.</span></span> <span data-ttu-id="6099b-106">Essa é uma função membro auxiliar interna.</span><span class="sxs-lookup"><span data-stu-id="6099b-106">This is an internal helper member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="6099b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6099b-107">Syntax</span></span>


```C++
virtual HRESULT GetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="6099b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6099b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6099b-109">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="6099b-109">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="6099b-110">Ponteiro para o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="6099b-110">Pointer to the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6099b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6099b-111">Return value</span></span>

<span data-ttu-id="6099b-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6099b-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6099b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6099b-113">Remarks</span></span>

<span data-ttu-id="6099b-114">Essa função de membro deve ser substituída na classe derivada para retornar o retângulo de destino mantido pelo processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6099b-114">This member function must be overridden in the derived class to return the target rectangle held by the video renderer.</span></span> <span data-ttu-id="6099b-115">Ele é chamado das seguintes funções de membro [**CBaseControlVideo**](cbasecontrolvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="6099b-115">It is called from the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="6099b-116">**CBaseControlVideo::GetDestinationPosition**</span><span class="sxs-lookup"><span data-stu-id="6099b-116">**CBaseControlVideo::GetDestinationPosition**</span></span>](cbasecontrolvideo-getdestinationposition.md)
-   [<span data-ttu-id="6099b-117">**CBaseControlVideo::p UT \_ DestinationLeft**</span><span class="sxs-lookup"><span data-stu-id="6099b-117">**CBaseControlVideo::put\_DestinationLeft**</span></span>](cbasecontrolvideo-put-destinationleft.md)
-   [<span data-ttu-id="6099b-118">**CBaseControlVideo:: obter \_ DestinationLeft**</span><span class="sxs-lookup"><span data-stu-id="6099b-118">**CBaseControlVideo::get\_DestinationLeft**</span></span>](cbasecontrolvideo-get-destinationleft.md)
-   [<span data-ttu-id="6099b-119">**CBaseControlVideo::p UT \_ DestinationWidth**</span><span class="sxs-lookup"><span data-stu-id="6099b-119">**CBaseControlVideo::put\_DestinationWidth**</span></span>](cbasecontrolvideo-put-destinationwidth.md)
-   [<span data-ttu-id="6099b-120">**CBaseControlVideo:: obter \_ DestinationWidth**</span><span class="sxs-lookup"><span data-stu-id="6099b-120">**CBaseControlVideo::get\_DestinationWidth**</span></span>](cbasecontrolvideo-get-destinationwidth.md)
-   [<span data-ttu-id="6099b-121">**CBaseControlVideo::p UT \_ DestinationTop**</span><span class="sxs-lookup"><span data-stu-id="6099b-121">**CBaseControlVideo::put\_DestinationTop**</span></span>](cbasecontrolvideo-put-destinationtop.md)
-   [<span data-ttu-id="6099b-122">**CBaseControlVideo:: obter \_ DestinationTop**</span><span class="sxs-lookup"><span data-stu-id="6099b-122">**CBaseControlVideo::get\_DestinationTop**</span></span>](cbasecontrolvideo-get-destinationtop.md)
-   [<span data-ttu-id="6099b-123">**CBaseControlVideo::p UT \_ DestinationHeight**</span><span class="sxs-lookup"><span data-stu-id="6099b-123">**CBaseControlVideo::put\_DestinationHeight**</span></span>](cbasecontrolvideo-put-destinationheight.md)
-   [<span data-ttu-id="6099b-124">**CBaseControlVideo:: obter \_ DestinationHeight**</span><span class="sxs-lookup"><span data-stu-id="6099b-124">**CBaseControlVideo::get\_DestinationHeight**</span></span>](cbasecontrolvideo-get-destinationheight.md)

<span data-ttu-id="6099b-125">O exemplo a seguir demonstra uma implementação dessa função em uma classe derivada.</span><span class="sxs-lookup"><span data-stu-id="6099b-125">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return the current destination rectangle.
HRESULT CVideoText::GetTargetRect(RECT *pTargetRect)
{
    ASSERT(pTargetRect);
    m_pRenderer->m_DrawImage.GetTargetRect(pTargetRect);
    return NOERROR;
}
```



<span data-ttu-id="6099b-126">Neste exemplo, CVideoText é uma classe derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer mantém um objeto de uma classe derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md), e o membro de \_ dados da DrawImage m, definido na classe derivada, mantém um objeto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="6099b-126">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6099b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6099b-127">Requirements</span></span>



| <span data-ttu-id="6099b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6099b-128">Requirement</span></span> | <span data-ttu-id="6099b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6099b-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6099b-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6099b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6099b-131"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6099b-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6099b-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6099b-132">Library</span></span><br/> | <dl> <span data-ttu-id="6099b-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6099b-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6099b-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6099b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6099b-135">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="6099b-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




