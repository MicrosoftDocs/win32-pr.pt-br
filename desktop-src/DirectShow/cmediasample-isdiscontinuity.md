---
description: 'O método IsDiscontinuity determina se este exemplo representa uma interrupção no fluxo de dados. Esse método implementa o método IMediaSample:: IsDiscontinuity.'
ms.assetid: 125b4a86-bd26-4539-a9ab-281f1aed1836
title: Método CMediaSample. IsDiscontinuity (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e222ea813793dd537c8623f74403baed9a320a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755349"
---
# <a name="cmediasampleisdiscontinuity-method"></a><span data-ttu-id="d337f-104">Método CMediaSample. IsDiscontinuity</span><span class="sxs-lookup"><span data-stu-id="d337f-104">CMediaSample.IsDiscontinuity method</span></span>

<span data-ttu-id="d337f-105">O `IsDiscontinuity` método determina se este exemplo representa uma interrupção no fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="d337f-105">The `IsDiscontinuity` method determines if this sample represents a break in the data stream.</span></span> <span data-ttu-id="d337f-106">Esse método implementa o método [**IMediaSample:: IsDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="d337f-106">This method implements the [**IMediaSample::IsDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d337f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d337f-107">Syntax</span></span>


```C++
HRESULT IsDiscontinuity();
```



## <a name="parameters"></a><span data-ttu-id="d337f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d337f-108">Parameters</span></span>

<span data-ttu-id="d337f-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d337f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d337f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d337f-110">Return value</span></span>

<span data-ttu-id="d337f-111">Retornará S \_ OK se o exemplo for uma interrupção no fluxo de dados e, \_ caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="d337f-111">Returns S\_OK if the sample is a break in the data stream, and S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d337f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d337f-112">Remarks</span></span>

<span data-ttu-id="d337f-113">A variável de membro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) especifica essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d337f-113">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d337f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d337f-114">Requirements</span></span>



| <span data-ttu-id="d337f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d337f-115">Requirement</span></span> | <span data-ttu-id="d337f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d337f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d337f-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d337f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d337f-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d337f-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d337f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d337f-119">Library</span></span><br/> | <dl> <span data-ttu-id="d337f-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d337f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d337f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d337f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d337f-122">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="d337f-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




