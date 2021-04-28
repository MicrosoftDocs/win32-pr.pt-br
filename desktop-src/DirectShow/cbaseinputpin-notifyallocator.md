---
description: 'Método CBaseInputPin. NotifyAllocator – o método NotifyAllocator especifica um alocador para a conexão. Esse método implementa o método IMemInputPin:: NotifyAllocator.'
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: Método CBaseInputPin. NotifyAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c63e448d0cf2d287a441a4983f6a2e06bd9b8151
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099706"
---
# <a name="cbaseinputpinnotifyallocator-method"></a><span data-ttu-id="6249d-104">Método CBaseInputPin. NotifyAllocator</span><span class="sxs-lookup"><span data-stu-id="6249d-104">CBaseInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="6249d-105">O `NotifyAllocator` método especifica um alocador para a conexão.</span><span class="sxs-lookup"><span data-stu-id="6249d-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="6249d-106">Esse método implementa o método [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) .</span><span class="sxs-lookup"><span data-stu-id="6249d-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6249d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6249d-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="6249d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6249d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6249d-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="6249d-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="6249d-110">Ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador.</span><span class="sxs-lookup"><span data-stu-id="6249d-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="6249d-111">*bReadOnly*</span><span class="sxs-lookup"><span data-stu-id="6249d-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="6249d-112">Sinalizador que especifica se os exemplos deste alocador são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6249d-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="6249d-113">Se **for true**, os exemplos serão somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6249d-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6249d-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6249d-114">Return value</span></span>

<span data-ttu-id="6249d-115">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6249d-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6249d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6249d-116">Remarks</span></span>

<span data-ttu-id="6249d-117">Durante a conexão do PIN, o pino de saída escolhe um alocador e chama esse método para notificar o PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="6249d-117">During the pin connection, the output pin chooses an allocator and calls this method to notify the input pin.</span></span> <span data-ttu-id="6249d-118">O pino de saída pode usar o alocador que o PIN de entrada propôs no método [**IMemInputPin:: Getalocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) ou pode fornecer seu próprio alocador.</span><span class="sxs-lookup"><span data-stu-id="6249d-118">The output pin can use the allocator that the input pin proposed in the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method, or it can provide its own allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="6249d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6249d-119">Requirements</span></span>



| <span data-ttu-id="6249d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6249d-120">Requirement</span></span> | <span data-ttu-id="6249d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6249d-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6249d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6249d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6249d-123"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6249d-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6249d-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6249d-124">Library</span></span><br/> | <dl> <span data-ttu-id="6249d-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6249d-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6249d-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6249d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6249d-127">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="6249d-127">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




