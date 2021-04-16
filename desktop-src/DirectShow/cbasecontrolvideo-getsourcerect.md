---
description: O método GetSourceRect recupera o retângulo de origem. Esse é um método interno.
ms.assetid: 51028b79-6aab-4abc-8ee8-2965bda9d191
title: Método CBaseControlVideo. GetSourceRect (Ctlutil. h)
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
ms.openlocfilehash: e57a5beda7b147e952ecbb26c96df5f7e372e6d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757898"
---
# <a name="cbasecontrolvideogetsourcerect-method"></a><span data-ttu-id="eb3fe-104">Método CBaseControlVideo. GetSourceRect</span><span class="sxs-lookup"><span data-stu-id="eb3fe-104">CBaseControlVideo.GetSourceRect method</span></span>

<span data-ttu-id="eb3fe-105">O `GetSourceRect` método recupera o retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="eb3fe-105">The `GetSourceRect` method retrieves the source rectangle.</span></span> <span data-ttu-id="eb3fe-106">Esse é um método interno.</span><span class="sxs-lookup"><span data-stu-id="eb3fe-106">This is an internal method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb3fe-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb3fe-107">Syntax</span></span>


```C++
virtual HRESULT GetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="eb3fe-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb3fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb3fe-109">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="eb3fe-109">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="eb3fe-110">Ponteiro para o retângulo de origem recuperado.</span><span class="sxs-lookup"><span data-stu-id="eb3fe-110">Pointer to the retrieved source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb3fe-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb3fe-111">Return value</span></span>

<span data-ttu-id="eb3fe-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eb3fe-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb3fe-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb3fe-113">Remarks</span></span>

<span data-ttu-id="eb3fe-114">Essa função de membro deve ser substituída na classe derivada para retornar o retângulo de origem mantido pelo processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="eb3fe-114">This member function must be overridden in the derived class to return the source rectangle held by the video renderer.</span></span> <span data-ttu-id="eb3fe-115">Ele é chamado das seguintes funções de membro [**CBaseControlVideo**](cbasecontrolvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="eb3fe-115">It is called from the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="eb3fe-116">**CBaseControlVideo::GetSourcePosition**</span><span class="sxs-lookup"><span data-stu-id="eb3fe-116">**CBaseControlVideo::GetSourcePosition**</span></span>](cbasecontrolvideo-getsourceposition.md)
-   [<span data-ttu-id="eb3fe-117">**CBaseControlVideo::p UT \_ SourceLeft**</span><span class="sxs-lookup"><span data-stu-id="eb3fe-117">**CBaseControlVideo::put\_SourceLeft**</span></span>](cbasecontrolvideo-put-sourceleft.md)
-   [<span data-ttu-id="eb3fe-118">**CBaseControlVideo:: obter \_ SourceLeft**</span><span class="sxs-lookup"><span data-stu-id="eb3fe-118">**CBaseControlVideo::get\_SourceLeft**</span></span>](cbasecontrolvideo-get-sourceleft.md)
-   [<span data-ttu-id="eb3fe-119">**CBaseControlVideo::p UT \_ SourceWidth**</span><span class="sxs-lookup"><span data-stu-id="eb3fe-119">**CBaseControlVideo::put\_SourceWidth**</span></span>](cbasecontrolvideo-put-sourcewidth.md)
-   [<span data-ttu-id="eb3fe-120">**CBaseControlVideo:: obter \_ SourceWidth**</span><span class="sxs-lookup"><span data-stu-id="eb3fe-120">**CBaseControlVideo::get\_SourceWidth**</span></span>](cbasecontrolvideo-get-sourcewidth.md)
-   [<span data-ttu-id="eb3fe-121">**CBaseControlVideo::p UT \_ SourceTop**</span><span class="sxs-lookup"><span data-stu-id="eb3fe-121">**CBaseControlVideo::put\_SourceTop**</span></span>](cbasecontrolvideo-put-sourcetop.md)
-   [<span data-ttu-id="eb3fe-122">**CBaseControlVideo:: obter \_ SourceTop**</span><span class="sxs-lookup"><span data-stu-id="eb3fe-122">**CBaseControlVideo::get\_SourceTop**</span></span>](cbasecontrolvideo-get-sourcetop.md)
-   [<span data-ttu-id="eb3fe-123">**CBaseControlVideo::p UT \_ SourceHeight**</span><span class="sxs-lookup"><span data-stu-id="eb3fe-123">**CBaseControlVideo::put\_SourceHeight**</span></span>](cbasecontrolvideo-put-sourceheight.md)
-   [<span data-ttu-id="eb3fe-124">**CBaseControlVideo:: obter \_ SourceHeight**</span><span class="sxs-lookup"><span data-stu-id="eb3fe-124">**CBaseControlVideo::get\_SourceHeight**</span></span>](cbasecontrolvideo-get-sourceheight.md)

<span data-ttu-id="eb3fe-125">O exemplo a seguir demonstra uma implementação dessa função em uma classe derivada.</span><span class="sxs-lookup"><span data-stu-id="eb3fe-125">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return the current source rectangle
HRESULT CVideoText::GetSourceRect(RECT *pSourceRect)
{
    ASSERT(pSourceRect);
    m_pRenderer->m_DrawImage.GetSourceRect(pSourceRect);
    return NOERROR;
}
```



<span data-ttu-id="eb3fe-126">Neste exemplo, CVideoText é uma classe derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer mantém um objeto de uma classe derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md), e o membro de \_ dados da DrawImage m, definido na classe derivada, mantém um objeto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="eb3fe-126">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb3fe-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb3fe-127">Requirements</span></span>



| <span data-ttu-id="eb3fe-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb3fe-128">Requirement</span></span> | <span data-ttu-id="eb3fe-129">Valor</span><span class="sxs-lookup"><span data-stu-id="eb3fe-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb3fe-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb3fe-130">Header</span></span><br/>  | <dl> <span data-ttu-id="eb3fe-131"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb3fe-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eb3fe-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb3fe-132">Library</span></span><br/> | <dl> <span data-ttu-id="eb3fe-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="eb3fe-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb3fe-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb3fe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb3fe-135">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="eb3fe-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




