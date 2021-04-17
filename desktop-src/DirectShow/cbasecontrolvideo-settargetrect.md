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
# <a name="cbasecontrolvideosettargetrect-method"></a><span data-ttu-id="4ead9-104">Método CBaseControlVideo. SetTargetRect</span><span class="sxs-lookup"><span data-stu-id="4ead9-104">CBaseControlVideo.SetTargetRect method</span></span>

<span data-ttu-id="4ead9-105">O `SetTargetRect` método define o retângulo de destino atual (virtual puro).</span><span class="sxs-lookup"><span data-stu-id="4ead9-105">The `SetTargetRect` method sets the current target rectangle (pure virtual).</span></span> <span data-ttu-id="4ead9-106">Essa é uma função de membro interna que é chamada quando o retângulo de destino é alterado.</span><span class="sxs-lookup"><span data-stu-id="4ead9-106">This is an internal member function that gets called when the destination rectangle changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ead9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ead9-107">Syntax</span></span>


```C++
virtual HRESULT SetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="4ead9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ead9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ead9-109">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="4ead9-109">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="4ead9-110">Ponteiro para o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="4ead9-110">Pointer to the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ead9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4ead9-111">Return value</span></span>

<span data-ttu-id="4ead9-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4ead9-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ead9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ead9-113">Remarks</span></span>

<span data-ttu-id="4ead9-114">Classes derivadas devem substituir isso para saber quando o retângulo de destino é alterado.</span><span class="sxs-lookup"><span data-stu-id="4ead9-114">Derived classes should override this to know when the destination rectangle changes.</span></span> <span data-ttu-id="4ead9-115">Ele é chamado a partir das seguintes funções de membro.</span><span class="sxs-lookup"><span data-stu-id="4ead9-115">It is called from the following member functions.</span></span>

-   [<span data-ttu-id="4ead9-116">**CBaseControlVideo::SetDestinationPosition**</span><span class="sxs-lookup"><span data-stu-id="4ead9-116">**CBaseControlVideo::SetDestinationPosition**</span></span>](cbasecontrolvideo-setdestinationposition.md)
-   [<span data-ttu-id="4ead9-117">**CBaseControlVideo::p UT \_ DestinationLeft**</span><span class="sxs-lookup"><span data-stu-id="4ead9-117">**CBaseControlVideo::put\_DestinationLeft**</span></span>](cbasecontrolvideo-put-destinationleft.md)
-   [<span data-ttu-id="4ead9-118">**CBaseControlVideo::p UT \_ DestinationWidth**</span><span class="sxs-lookup"><span data-stu-id="4ead9-118">**CBaseControlVideo::put\_DestinationWidth**</span></span>](cbasecontrolvideo-put-destinationwidth.md)
-   [<span data-ttu-id="4ead9-119">**CBaseControlVideo::p UT \_ DestinationTop**</span><span class="sxs-lookup"><span data-stu-id="4ead9-119">**CBaseControlVideo::put\_DestinationTop**</span></span>](cbasecontrolvideo-put-destinationtop.md)
-   [<span data-ttu-id="4ead9-120">**CBaseControlVideo::p UT \_ DestinationHeight**</span><span class="sxs-lookup"><span data-stu-id="4ead9-120">**CBaseControlVideo::put\_DestinationHeight**</span></span>](cbasecontrolvideo-put-destinationheight.md)

<span data-ttu-id="4ead9-121">O exemplo a seguir demonstra uma implementação dessa função em uma classe derivada.</span><span class="sxs-lookup"><span data-stu-id="4ead9-121">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
HRESULT CVideoText::SetTargetRect(RECT *pTargetRect)
{
    m_pRenderer->m_DrawImage.SetTargetRect(pTargetRect);
    return NOERROR;
}
```



<span data-ttu-id="4ead9-122">Neste exemplo, CVideoText é uma classe derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer mantém um objeto de uma classe derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md), e o membro de \_ dados da DrawImage m, definido na classe derivada, mantém um objeto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="4ead9-122">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ead9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ead9-123">Requirements</span></span>



| <span data-ttu-id="4ead9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ead9-124">Requirement</span></span> | <span data-ttu-id="4ead9-125">Valor</span><span class="sxs-lookup"><span data-stu-id="4ead9-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ead9-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ead9-126">Header</span></span><br/>  | <dl> <span data-ttu-id="4ead9-127"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ead9-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4ead9-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4ead9-128">Library</span></span><br/> | <dl> <span data-ttu-id="4ead9-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4ead9-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ead9-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ead9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ead9-131">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="4ead9-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




