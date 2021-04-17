---
description: 'O método GetAllocatorRequirements recupera as propriedades de alocador solicitadas pelo PIN. Esse método implementa o método IMemInputPin:: GetAllocatorRequirements.'
ms.assetid: 1355facc-f863-44b2-9284-8f06f62d39a2
title: Método CTransInPlaceInputPin. GetAllocatorRequirements (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa176cd5da0317821996593e19bb90396e82224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758443"
---
# <a name="ctransinplaceinputpingetallocatorrequirements-method"></a><span data-ttu-id="e25f4-104">Método CTransInPlaceInputPin. GetAllocatorRequirements</span><span class="sxs-lookup"><span data-stu-id="e25f4-104">CTransInPlaceInputPin.GetAllocatorRequirements method</span></span>

<span data-ttu-id="e25f4-105">O `GetAllocatorRequirements` método recupera as propriedades de alocador solicitadas pelo PIN.</span><span class="sxs-lookup"><span data-stu-id="e25f4-105">The `GetAllocatorRequirements` method retrieves the allocator properties requested by the pin.</span></span> <span data-ttu-id="e25f4-106">Esse método implementa o método [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) .</span><span class="sxs-lookup"><span data-stu-id="e25f4-106">This method implements the [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e25f4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e25f4-107">Syntax</span></span>


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="e25f4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e25f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e25f4-109">*pProps*</span><span class="sxs-lookup"><span data-stu-id="e25f4-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="e25f4-110">Ponteiro para uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , que é preenchida com os requisitos.</span><span class="sxs-lookup"><span data-stu-id="e25f4-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure, which is filled in with the requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e25f4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e25f4-111">Return value</span></span>

<span data-ttu-id="e25f4-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e25f4-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e25f4-113">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e25f4-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="e25f4-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e25f4-114">Return code</span></span>                                                                               | <span data-ttu-id="e25f4-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="e25f4-115">Description</span></span>                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e25f4-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e25f4-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="e25f4-117">Sucesso</span><span class="sxs-lookup"><span data-stu-id="e25f4-117">Success</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="e25f4-118"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="e25f4-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="e25f4-119">O pino de saída não está conectado ou o pino de entrada downstream não oferece suporte ao método.</span><span class="sxs-lookup"><span data-stu-id="e25f4-119">The output pin is not connected, or the downstream input pin does not support the method.</span></span><br/> |
| <dl> <span data-ttu-id="e25f4-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="e25f4-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="e25f4-121">Argumento de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="e25f4-121">**NULL** pointer argument</span></span><br/>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="e25f4-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="e25f4-122">Remarks</span></span>

<span data-ttu-id="e25f4-123">Se o pino de saída estiver conectado, esse método passará a chamada para o pino de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="e25f4-123">If the output pin is connected, this method passes the call to the downstream input pin.</span></span> <span data-ttu-id="e25f4-124">Caso contrário, retornará E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="e25f4-124">Otherwise, it returns E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e25f4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e25f4-125">Requirements</span></span>



| <span data-ttu-id="e25f4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e25f4-126">Requirement</span></span> | <span data-ttu-id="e25f4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e25f4-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e25f4-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e25f4-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e25f4-129"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e25f4-129"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e25f4-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e25f4-130">Library</span></span><br/> | <dl> <span data-ttu-id="e25f4-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e25f4-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e25f4-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e25f4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e25f4-133">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="e25f4-133">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




