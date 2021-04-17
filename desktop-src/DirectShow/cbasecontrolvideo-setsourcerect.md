---
description: O método SetSourceRect define o retângulo de vídeo de origem atual (virtual puro). Essa é uma função de membro interna que é chamada quando o retângulo de origem é alterado.
ms.assetid: 13bb594b-b154-40a2-ad00-f1e86781074d
title: Método CBaseControlVideo. SetSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e3be6cc3819e1452fd196d4906377204a6e90bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811764"
---
# <a name="cbasecontrolvideosetsourcerect-method"></a><span data-ttu-id="af2b6-104">Método CBaseControlVideo. SetSourceRect</span><span class="sxs-lookup"><span data-stu-id="af2b6-104">CBaseControlVideo.SetSourceRect method</span></span>

<span data-ttu-id="af2b6-105">O `SetSourceRect` método define o retângulo de vídeo de origem atual (virtual puro).</span><span class="sxs-lookup"><span data-stu-id="af2b6-105">The `SetSourceRect` method sets the current source video rectangle (pure virtual).</span></span> <span data-ttu-id="af2b6-106">Essa é uma função de membro interna que é chamada quando o retângulo de origem é alterado.</span><span class="sxs-lookup"><span data-stu-id="af2b6-106">This is an internal member function that gets called when the source rectangle changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="af2b6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af2b6-107">Syntax</span></span>


```C++
virtual HRESULT SetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="af2b6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af2b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af2b6-109">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="af2b6-109">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="af2b6-110">Ponteiro para o retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="af2b6-110">Pointer to the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af2b6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af2b6-111">Return value</span></span>

<span data-ttu-id="af2b6-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="af2b6-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af2b6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="af2b6-113">Remarks</span></span>

<span data-ttu-id="af2b6-114">Classes derivadas devem substituir essa função de membro para saber quando o retângulo de origem é alterado.</span><span class="sxs-lookup"><span data-stu-id="af2b6-114">Derived classes should override this member function to know when the source rectangle changes.</span></span> <span data-ttu-id="af2b6-115">Ele é chamado a partir das seguintes funções de membro.</span><span class="sxs-lookup"><span data-stu-id="af2b6-115">It is called from the following member functions.</span></span>

-   [<span data-ttu-id="af2b6-116">**CBaseControlVideo::SetSourcePosition**</span><span class="sxs-lookup"><span data-stu-id="af2b6-116">**CBaseControlVideo::SetSourcePosition**</span></span>](cbasecontrolvideo-setsourceposition.md)
-   [<span data-ttu-id="af2b6-117">**CBaseControlVideo::p UT \_ SourceLeft**</span><span class="sxs-lookup"><span data-stu-id="af2b6-117">**CBaseControlVideo::put\_SourceLeft**</span></span>](cbasecontrolvideo-put-sourceleft.md)
-   [<span data-ttu-id="af2b6-118">**CBaseControlVideo::p UT \_ SourceWidth**</span><span class="sxs-lookup"><span data-stu-id="af2b6-118">**CBaseControlVideo::put\_SourceWidth**</span></span>](cbasecontrolvideo-put-sourcewidth.md)
-   [<span data-ttu-id="af2b6-119">**CBaseControlVideo::p UT \_ SourceTop**</span><span class="sxs-lookup"><span data-stu-id="af2b6-119">**CBaseControlVideo::put\_SourceTop**</span></span>](cbasecontrolvideo-put-sourcetop.md)
-   [<span data-ttu-id="af2b6-120">**CBaseControlVideo::p UT \_ SourceHeight**</span><span class="sxs-lookup"><span data-stu-id="af2b6-120">**CBaseControlVideo::put\_SourceHeight**</span></span>](cbasecontrolvideo-put-sourceheight.md)

<span data-ttu-id="af2b6-121">O exemplo a seguir demonstra uma implementação dessa função em uma classe derivada.</span><span class="sxs-lookup"><span data-stu-id="af2b6-121">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
HRESULT CVideoText::SetSourceRect(RECT *pSourceRect)
{
    m_pRenderer->m_DrawImage.SetSourceRect(pSourceRect);
    return NOERROR;
}
```



<span data-ttu-id="af2b6-122">Neste exemplo, CVideoText é uma classe derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer mantém um objeto de uma classe derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md), e o membro de \_ dados da DrawImage m, definido na classe derivada, mantém um objeto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="af2b6-122">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="af2b6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af2b6-123">Requirements</span></span>



| <span data-ttu-id="af2b6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="af2b6-124">Requirement</span></span> | <span data-ttu-id="af2b6-125">Valor</span><span class="sxs-lookup"><span data-stu-id="af2b6-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af2b6-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af2b6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="af2b6-127"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af2b6-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="af2b6-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af2b6-128">Library</span></span><br/> | <dl> <span data-ttu-id="af2b6-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="af2b6-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af2b6-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="af2b6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af2b6-131">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="af2b6-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




