---
description: O método setalocador especifica um alocador para a conexão.
ms.assetid: 6b8e80f9-3b0d-498f-b1b0-bae491c25e81
title: Método CTransInPlaceOutputPin. setalocador (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.SetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aacc2680bebcdd7de74f6f357380066a8fd37f1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748185"
---
# <a name="ctransinplaceoutputpinsetallocator-method"></a><span data-ttu-id="a2ee0-103">Método CTransInPlaceOutputPin. setalocador</span><span class="sxs-lookup"><span data-stu-id="a2ee0-103">CTransInPlaceOutputPin.SetAllocator method</span></span>

<span data-ttu-id="a2ee0-104">O `SetAllocator` método especifica um alocador para a conexão.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-104">The `SetAllocator` method specifies an allocator for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2ee0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2ee0-105">Syntax</span></span>


```C++
void SetAllocator(
   IMemAllocator *pAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="a2ee0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2ee0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2ee0-107">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="a2ee0-107">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="a2ee0-108">Ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2ee0-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2ee0-109">Return value</span></span>

<span data-ttu-id="a2ee0-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2ee0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2ee0-111">Remarks</span></span>

<span data-ttu-id="a2ee0-112">O pino de saída para esse filtro nunca fornece um alocador.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-112">The output pin for this filter never provides an allocator.</span></span> <span data-ttu-id="a2ee0-113">Esse método especifica o alocador para o pino de saída.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-113">This method specifies the allocator for the output pin.</span></span> <span data-ttu-id="a2ee0-114">Ele define o valor da variável de membro [**CBaseOutputPin:: m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="a2ee0-114">It sets the value of the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2ee0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2ee0-115">Requirements</span></span>



| <span data-ttu-id="a2ee0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2ee0-116">Requirement</span></span> | <span data-ttu-id="a2ee0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a2ee0-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ee0-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2ee0-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a2ee0-119"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2ee0-119"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a2ee0-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a2ee0-120">Library</span></span><br/> | <dl> <span data-ttu-id="a2ee0-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a2ee0-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2ee0-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2ee0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2ee0-123">**Classe CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="a2ee0-123">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




