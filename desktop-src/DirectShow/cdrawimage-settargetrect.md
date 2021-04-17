---
description: O método SetTargetRect define o retângulo de destino.
ms.assetid: 033f8bae-e63d-4be0-8dd0-715cc1229392
title: Método CDrawImage. SetTargetRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4513b6aeda16d19476769290a6139f91b2fd1f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755352"
---
# <a name="cdrawimagesettargetrect-method"></a><span data-ttu-id="a3714-103">Método CDrawImage. SetTargetRect</span><span class="sxs-lookup"><span data-stu-id="a3714-103">CDrawImage.SetTargetRect method</span></span>

<span data-ttu-id="a3714-104">O `SetTargetRect` método define o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="a3714-104">The `SetTargetRect` method sets the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3714-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3714-105">Syntax</span></span>


```C++
void SetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a><span data-ttu-id="a3714-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3714-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3714-107">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="a3714-107">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="a3714-108">Ponteiro para uma estrutura **Rect** que define o novo retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="a3714-108">Pointer to a **RECT** structure that defines the new target rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3714-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3714-109">Return value</span></span>

<span data-ttu-id="a3714-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a3714-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3714-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3714-111">Remarks</span></span>

<span data-ttu-id="a3714-112">O filtro proprietário deve chamar esse método se o retângulo de origem for alterado; por exemplo, em resposta a uma chamada [**IBasicVideo:: SetDestinationPosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) .</span><span class="sxs-lookup"><span data-stu-id="a3714-112">The owning filter should call this method if the source rectangle changes; for example, in response to an [**IBasicVideo::SetDestinationPosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) call.</span></span>

<span data-ttu-id="a3714-113">Antes de chamar esse método, valide o retângulo fornecido em *pTargetRect*, em relação à janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a3714-113">Before calling this method, validate the rectangle given in *pTargetRect*, relative to the video window.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3714-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3714-114">Requirements</span></span>



| <span data-ttu-id="a3714-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3714-115">Requirement</span></span> | <span data-ttu-id="a3714-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a3714-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3714-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a3714-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a3714-118"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3714-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a3714-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a3714-119">Library</span></span><br/> | <dl> <span data-ttu-id="a3714-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a3714-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3714-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3714-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3714-122">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="a3714-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




