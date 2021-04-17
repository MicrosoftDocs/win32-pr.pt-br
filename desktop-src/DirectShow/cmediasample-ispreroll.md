---
description: 'O método IsPreroll determina se este exemplo é uma amostra de preversão. Um exemplo de preroll não deve ser exibido. Esse método implementa o método IMediaSample:: IsPreroll.'
ms.assetid: fbcf7aab-473c-49c1-9a8f-4a619f4e28f4
title: Método CMediaSample. IsPreroll (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40cf8fd6a1adb5186309f47da0f0ae3dc30412a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787405"
---
# <a name="cmediasampleispreroll-method"></a><span data-ttu-id="af459-105">Método CMediaSample. IsPreroll</span><span class="sxs-lookup"><span data-stu-id="af459-105">CMediaSample.IsPreroll method</span></span>

<span data-ttu-id="af459-106">O `IsPreroll` método determina se este exemplo é uma amostra de preversão.</span><span class="sxs-lookup"><span data-stu-id="af459-106">The `IsPreroll` method determines if this sample is a preroll sample.</span></span> <span data-ttu-id="af459-107">Um exemplo de preroll não deve ser exibido.</span><span class="sxs-lookup"><span data-stu-id="af459-107">A preroll sample should not be displayed.</span></span> <span data-ttu-id="af459-108">Esse método implementa o método [**IMediaSample:: IsPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) .</span><span class="sxs-lookup"><span data-stu-id="af459-108">This method implements the [**IMediaSample::IsPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="af459-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af459-109">Syntax</span></span>


```C++
HRESULT IsPreroll();
```



## <a name="parameters"></a><span data-ttu-id="af459-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af459-110">Parameters</span></span>

<span data-ttu-id="af459-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="af459-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="af459-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af459-112">Return value</span></span>

<span data-ttu-id="af459-113">Retornará S \_ OK se o exemplo for um exemplo de preroll e, \_ caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="af459-113">Returns S\_OK if the sample is a preroll sample, and S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="af459-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="af459-114">Remarks</span></span>

<span data-ttu-id="af459-115">A variável de membro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) especifica essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="af459-115">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="af459-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af459-116">Requirements</span></span>



| <span data-ttu-id="af459-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="af459-117">Requirement</span></span> | <span data-ttu-id="af459-118">Valor</span><span class="sxs-lookup"><span data-stu-id="af459-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af459-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af459-119">Header</span></span><br/>  | <dl> <span data-ttu-id="af459-120"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af459-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="af459-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af459-121">Library</span></span><br/> | <dl> <span data-ttu-id="af459-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="af459-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af459-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="af459-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af459-124">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="af459-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




