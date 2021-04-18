---
description: O \_ método Get AvgFrameRate calcula e recupera a taxa média de quadros obtida.
ms.assetid: f36fc020-8c1a-491f-9f55-18265fde8bf8
title: Método de CBaseVideoRenderer.get_AvgFrameRate (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgFrameRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d8fff53f3d56676805eca9029670d51210ef2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751902"
---
# <a name="cbasevideorendererget_avgframerate-method"></a><span data-ttu-id="c7ed4-103">CBaseVideoRenderer. obter \_ método AvgFrameRate</span><span class="sxs-lookup"><span data-stu-id="c7ed4-103">CBaseVideoRenderer.get\_AvgFrameRate method</span></span>

<span data-ttu-id="c7ed4-104">O `get_AvgFrameRate` método calcula e recupera a taxa média de quadros obtida.</span><span class="sxs-lookup"><span data-stu-id="c7ed4-104">The `get_AvgFrameRate` method calculates and retrieves the average frame rate achieved.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7ed4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7ed4-105">Syntax</span></span>


```C++
HRESULT get_AvgFrameRate(
   int *piAvgFrameRate
);
```



## <a name="parameters"></a><span data-ttu-id="c7ed4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7ed4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7ed4-107">*piAvgFrameRate*</span><span class="sxs-lookup"><span data-stu-id="c7ed4-107">*piAvgFrameRate*</span></span> 
</dt> <dd>

<span data-ttu-id="c7ed4-108">Ponteiro para o número de quadros por segundo desde o início do streaming.</span><span class="sxs-lookup"><span data-stu-id="c7ed4-108">Pointer to the number of frames per second since streaming began.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7ed4-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7ed4-109">Return value</span></span>

<span data-ttu-id="c7ed4-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c7ed4-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7ed4-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7ed4-111">Remarks</span></span>

<span data-ttu-id="c7ed4-112">Essa função de membro implementa o método [**IQualProp:: get \_ AvgFrameRate**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) .</span><span class="sxs-lookup"><span data-stu-id="c7ed4-112">This member function implements the [**IQualProp::get\_AvgFrameRate**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7ed4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7ed4-113">Requirements</span></span>



| <span data-ttu-id="c7ed4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7ed4-114">Requirement</span></span> | <span data-ttu-id="c7ed4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c7ed4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7ed4-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7ed4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c7ed4-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7ed4-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c7ed4-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7ed4-118">Library</span></span><br/> | <dl> <span data-ttu-id="c7ed4-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c7ed4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7ed4-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7ed4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7ed4-121">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="c7ed4-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




