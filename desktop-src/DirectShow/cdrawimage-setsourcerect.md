---
description: O método SetSourceRect define o retângulo de origem.
ms.assetid: 982636fe-73ea-4f13-9f2b-7ae8df839ab1
title: Método CDrawImage. SetSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64fb8729b694d38eac2d6321f92904292d99bd38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756602"
---
# <a name="cdrawimagesetsourcerect-method"></a><span data-ttu-id="a7998-103">Método CDrawImage. SetSourceRect</span><span class="sxs-lookup"><span data-stu-id="a7998-103">CDrawImage.SetSourceRect method</span></span>

<span data-ttu-id="a7998-104">O `SetSourceRect` método define o retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="a7998-104">The `SetSourceRect` method sets the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7998-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7998-105">Syntax</span></span>


```C++
void SetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="a7998-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7998-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7998-107">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="a7998-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="a7998-108">Ponteiro para uma estrutura **Rect** que define o novo retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="a7998-108">Pointer to a **RECT** structure that defines the new source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7998-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a7998-109">Return value</span></span>

<span data-ttu-id="a7998-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a7998-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7998-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7998-111">Remarks</span></span>

<span data-ttu-id="a7998-112">O filtro proprietário deve chamar esse método se o retângulo de origem for alterado; por exemplo, em resposta a uma chamada [**IBasicVideo:: SetSourcePosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) .</span><span class="sxs-lookup"><span data-stu-id="a7998-112">The owning filter should call this method if the source rectangle changes; for example, in response to an [**IBasicVideo::SetSourcePosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) call.</span></span>

<span data-ttu-id="a7998-113">Valide o retângulo fornecido em *pSourceRect* antes de chamar esse método, para certificar-se de que ele não ultrapasse o tamanho do vídeo nativo.</span><span class="sxs-lookup"><span data-stu-id="a7998-113">Validate the rectangle given in *pSourceRect* before calling this method, to make sure it does not extend beyond the native video size.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7998-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7998-114">Requirements</span></span>



| <span data-ttu-id="a7998-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7998-115">Requirement</span></span> | <span data-ttu-id="a7998-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a7998-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7998-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7998-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a7998-118"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7998-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a7998-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a7998-119">Library</span></span><br/> | <dl> <span data-ttu-id="a7998-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a7998-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7998-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7998-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7998-122">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="a7998-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




