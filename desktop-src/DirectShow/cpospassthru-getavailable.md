---
description: 'O método GetAvailable recupera o intervalo de vezes em que a busca é eficiente. Esse método implementa o método IMediaSeeking:: GetAvailable.'
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: Método CPosPassThru. GetAvailable (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32dbba173caf933185602523dadcf71ce7ca3ef7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760756"
---
# <a name="cpospassthrugetavailable-method"></a><span data-ttu-id="bbae4-104">Método CPosPassThru. GetAvailable</span><span class="sxs-lookup"><span data-stu-id="bbae4-104">CPosPassThru.GetAvailable method</span></span>

<span data-ttu-id="bbae4-105">O `GetAvailable` método recupera o intervalo de vezes em que a busca é eficiente.</span><span class="sxs-lookup"><span data-stu-id="bbae4-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="bbae4-106">Esse método implementa o método [**IMediaSeeking:: GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .</span><span class="sxs-lookup"><span data-stu-id="bbae4-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbae4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbae4-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="bbae4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbae4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbae4-109">*pEarliest*</span><span class="sxs-lookup"><span data-stu-id="bbae4-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="bbae4-110">Ponteiro para uma variável que recebe a hora mais antiga para busca eficiente.</span><span class="sxs-lookup"><span data-stu-id="bbae4-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span>

</dd> <dt>

<span data-ttu-id="bbae4-111">*mais chapas*</span><span class="sxs-lookup"><span data-stu-id="bbae4-111">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="bbae4-112">Ponteiro para uma variável que recebe a hora mais recente para busca eficiente.</span><span class="sxs-lookup"><span data-stu-id="bbae4-112">Pointer to a variable that receives the latest time for efficient seeking.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbae4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bbae4-113">Return value</span></span>

<span data-ttu-id="bbae4-114">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="bbae4-114">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbae4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbae4-115">Requirements</span></span>



| <span data-ttu-id="bbae4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbae4-116">Requirement</span></span> | <span data-ttu-id="bbae4-117">Valor</span><span class="sxs-lookup"><span data-stu-id="bbae4-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbae4-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bbae4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="bbae4-119"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bbae4-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bbae4-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bbae4-120">Library</span></span><br/> | <dl> <span data-ttu-id="bbae4-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="bbae4-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbae4-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbae4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbae4-123">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="bbae4-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




