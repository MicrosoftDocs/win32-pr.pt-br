---
description: 'O método SetRate define a taxa de reprodução. Esse método implementa o método IMediaSeeking:: SetRate.'
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
ms.openlocfilehash: 718a38f3eff9cc1647d09cf142db784f53e4c755
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792559"
---
# <a name="csourceseekingsetrate-method"></a><span data-ttu-id="34025-104">Método CSourceSeeking. SetRate</span><span class="sxs-lookup"><span data-stu-id="34025-104">CSourceSeeking.SetRate method</span></span>

<span data-ttu-id="34025-105">O `SetRate` método define a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="34025-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="34025-106">Esse método implementa o método [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) .</span><span class="sxs-lookup"><span data-stu-id="34025-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="34025-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34025-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="34025-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34025-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34025-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="34025-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="34025-110">Taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="34025-110">Playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34025-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="34025-111">Return value</span></span>

<span data-ttu-id="34025-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="34025-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="34025-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="34025-113">Remarks</span></span>

<span data-ttu-id="34025-114">Esse método atualiza o valor da variável de membro [**CSourceSeeking:: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) e, em seguida, chama o método virtual puro [**CSourceSeeking:: disqueteira**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="34025-114">This method updates the value of the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="34025-115">O método não valida o parâmetro *drate* .</span><span class="sxs-lookup"><span data-stu-id="34025-115">The method does not validate the *dRate* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="34025-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34025-116">Requirements</span></span>



| <span data-ttu-id="34025-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="34025-117">Requirement</span></span> | <span data-ttu-id="34025-118">Valor</span><span class="sxs-lookup"><span data-stu-id="34025-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34025-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="34025-119">Header</span></span><br/>  | <dl> <span data-ttu-id="34025-120"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34025-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="34025-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="34025-121">Library</span></span><br/> | <dl> <span data-ttu-id="34025-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="34025-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34025-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="34025-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34025-124">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="34025-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




