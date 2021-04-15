---
description: 'O método getalocador recupera o alocador de memória proposto por esse PIN. Esse método implementa o método IMemInputPin:: getalocator.'
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: Método CBaseInputPin. getalocador (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 098738fc63ba1834b1eefb4b2518e3309db35c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747612"
---
# <a name="cbaseinputpingetallocator-method"></a><span data-ttu-id="3f3f6-104">Método CBaseInputPin. getalocador</span><span class="sxs-lookup"><span data-stu-id="3f3f6-104">CBaseInputPin.GetAllocator method</span></span>

<span data-ttu-id="3f3f6-105">O `GetAllocator` método recupera o alocador de memória proposto por esse PIN.</span><span class="sxs-lookup"><span data-stu-id="3f3f6-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="3f3f6-106">Esse método implementa o método [**IMemInputPin:: Getalocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) .</span><span class="sxs-lookup"><span data-stu-id="3f3f6-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f3f6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f3f6-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="3f3f6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f3f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f3f6-109">*ppAllocator*</span><span class="sxs-lookup"><span data-stu-id="3f3f6-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="3f3f6-110">Endereço de uma variável que recebe um ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador.</span><span class="sxs-lookup"><span data-stu-id="3f3f6-110">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f3f6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f3f6-111">Return value</span></span>

<span data-ttu-id="3f3f6-112">Retorna S \_ OK se for bem-sucedido ou um código de erro da função **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="3f3f6-112">Returns S\_OK if successful, or an error code from the **CoCreateInstance** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f3f6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f3f6-113">Remarks</span></span>

<span data-ttu-id="3f3f6-114">Esse método cria um objeto [**CMemAllocator**](cmemallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="3f3f6-114">This method creates a [**CMemAllocator**](cmemallocator.md) object.</span></span> <span data-ttu-id="3f3f6-115">Substitua esse método se o filtro usar um alocador de um PIN de downstream ou um alocador personalizado.</span><span class="sxs-lookup"><span data-stu-id="3f3f6-115">Override this method if your filter uses an allocator from a downstream pin, or a custom allocator.</span></span>

<span data-ttu-id="3f3f6-116">Se o método tiver sucesso, a interface **IMemAllocator** terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="3f3f6-116">If the method succeeds, the **IMemAllocator** interface has an outstanding reference count.</span></span> <span data-ttu-id="3f3f6-117">Certifique-se de liberá-lo quando terminar.</span><span class="sxs-lookup"><span data-stu-id="3f3f6-117">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f3f6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f3f6-118">Requirements</span></span>



| <span data-ttu-id="3f3f6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f3f6-119">Requirement</span></span> | <span data-ttu-id="3f3f6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3f3f6-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f3f6-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f3f6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3f3f6-122"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f3f6-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3f3f6-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f3f6-123">Library</span></span><br/> | <dl> <span data-ttu-id="3f3f6-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3f3f6-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f3f6-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f3f6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f3f6-126">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="3f3f6-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




