---
description: 'Método CSourceSeeking. SetRate-o método SetRate define a taxa de reprodução. Esse método implementa o método IMediaSeeking:: SetRate.'
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: Método CSourceSeeking. SetRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c37d9c94da4a59a2be9b7258881c5bb22b4aa4c5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098734"
---
# <a name="csourceseekingsetrate-method"></a><span data-ttu-id="80623-104">Método CSourceSeeking. SetRate</span><span class="sxs-lookup"><span data-stu-id="80623-104">CSourceSeeking.SetRate method</span></span>

<span data-ttu-id="80623-105">O `SetRate` método define a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="80623-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="80623-106">Esse método implementa o método [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) .</span><span class="sxs-lookup"><span data-stu-id="80623-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="80623-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80623-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="80623-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80623-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80623-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="80623-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="80623-110">Taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="80623-110">Playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80623-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="80623-111">Return value</span></span>

<span data-ttu-id="80623-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="80623-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="80623-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="80623-113">Remarks</span></span>

<span data-ttu-id="80623-114">Esse método atualiza o valor da variável de membro [**CSourceSeeking:: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) e, em seguida, chama o método virtual puro [**CSourceSeeking:: disqueteira**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="80623-114">This method updates the value of the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="80623-115">O método não valida o parâmetro *drate* .</span><span class="sxs-lookup"><span data-stu-id="80623-115">The method does not validate the *dRate* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="80623-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80623-116">Requirements</span></span>



| <span data-ttu-id="80623-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="80623-117">Requirement</span></span> | <span data-ttu-id="80623-118">Valor</span><span class="sxs-lookup"><span data-stu-id="80623-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80623-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="80623-119">Header</span></span><br/>  | <dl> <span data-ttu-id="80623-120"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80623-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="80623-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80623-121">Library</span></span><br/> | <dl> <span data-ttu-id="80623-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="80623-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80623-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="80623-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80623-124">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="80623-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




