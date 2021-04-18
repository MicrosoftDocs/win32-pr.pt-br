---
description: O \_ método Get FramesDrawn recupera a \_ variável de membro m cFramesDrawn, fornecendo o número de quadros desenhados desde o início do streaming.
ms.assetid: 486b5541-2952-47ce-944e-4efb8e5af9dd
title: Método de CBaseVideoRenderer.get_FramesDrawn (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDrawn
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec8254e06429022bf657322e98ab317475c82f90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759149"
---
# <a name="cbasevideorendererget_framesdrawn-method"></a><span data-ttu-id="21207-103">CBaseVideoRenderer. obter \_ método FramesDrawn</span><span class="sxs-lookup"><span data-stu-id="21207-103">CBaseVideoRenderer.get\_FramesDrawn method</span></span>

<span data-ttu-id="21207-104">O `get_FramesDrawn` método recupera a variável de membro **m \_ cFramesDrawn** , fornecendo o número de quadros desenhados desde o início do streaming.</span><span class="sxs-lookup"><span data-stu-id="21207-104">The `get_FramesDrawn` method retrieves the **m\_cFramesDrawn** member variable, giving the number of frames drawn since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="21207-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21207-105">Syntax</span></span>


```C++
HRESULT get_FramesDrawn(
   int *pcFramesDrawn
);
```



## <a name="parameters"></a><span data-ttu-id="21207-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21207-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21207-107">*pcFramesDrawn*</span><span class="sxs-lookup"><span data-stu-id="21207-107">*pcFramesDrawn*</span></span> 
</dt> <dd>

<span data-ttu-id="21207-108">Ponteiro para o número de quadros desenhados.</span><span class="sxs-lookup"><span data-stu-id="21207-108">Pointer to the number of frames drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21207-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="21207-109">Return value</span></span>

<span data-ttu-id="21207-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="21207-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="21207-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="21207-111">Remarks</span></span>

<span data-ttu-id="21207-112">Essa função de membro implementa o método [**IQualProp:: get \_ FramesDrawn**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn) .</span><span class="sxs-lookup"><span data-stu-id="21207-112">This member function implements the [**IQualProp::get\_FramesDrawn**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="21207-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21207-113">Requirements</span></span>



| <span data-ttu-id="21207-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="21207-114">Requirement</span></span> | <span data-ttu-id="21207-115">Valor</span><span class="sxs-lookup"><span data-stu-id="21207-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21207-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="21207-116">Header</span></span><br/>  | <dl> <span data-ttu-id="21207-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21207-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="21207-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="21207-118">Library</span></span><br/> | <dl> <span data-ttu-id="21207-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="21207-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21207-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="21207-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21207-121">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="21207-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




