---
description: O método CheckSizes verifica as propriedades de alocador em relação ao tipo de mídia atual.
ms.assetid: 040b4ed0-c1cc-4995-a0f8-86efa493f84b
title: Método CImageAllocator. CheckSizes (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CheckSizes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71184d4915911c29bff9d3a6fa9985942a4aaa44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786992"
---
# <a name="cimageallocatorchecksizes-method"></a><span data-ttu-id="f5cff-103">Método CImageAllocator. CheckSizes</span><span class="sxs-lookup"><span data-stu-id="f5cff-103">CImageAllocator.CheckSizes method</span></span>

<span data-ttu-id="f5cff-104">O `CheckSizes` método verifica as propriedades de alocador em relação ao tipo de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="f5cff-104">The `CheckSizes` method checks allocator properties against the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5cff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5cff-105">Syntax</span></span>


```C++
HRESULT CheckSizes(
   ALLOCATOR_PROPERTIES *pRequest
);
```



## <a name="parameters"></a><span data-ttu-id="f5cff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5cff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5cff-107">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="f5cff-107">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="f5cff-108">Ponteiro para uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que descreve as propriedades de alocador solicitadas.</span><span class="sxs-lookup"><span data-stu-id="f5cff-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that describes the requested allocator properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5cff-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5cff-109">Return value</span></span>

<span data-ttu-id="f5cff-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f5cff-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f5cff-111">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="f5cff-111">Possible values include the following.</span></span>



| <span data-ttu-id="f5cff-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f5cff-112">Return code</span></span>                                                                                           | <span data-ttu-id="f5cff-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5cff-113">Description</span></span>                                                                 |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5cff-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f5cff-114"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="f5cff-115">As propriedades solicitadas são compatíveis com o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="f5cff-115">The requested properties are compatible with the media type.</span></span><br/>     |
| <dl> <span data-ttu-id="f5cff-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f5cff-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="f5cff-117">As propriedades solicitadas não são compatíveis com o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="f5cff-117">The requested properties are not compatible with the media type.</span></span><br/> |
| <dl> <span data-ttu-id="f5cff-118"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="f5cff-118"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="f5cff-119">O PIN proprietário não está conectado.</span><span class="sxs-lookup"><span data-stu-id="f5cff-119">The owning pin is not connected.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="f5cff-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5cff-120">Remarks</span></span>

<span data-ttu-id="f5cff-121">Quando o método retornar, se o valor de retorno for S \_ OK, o membro **cbBuffer** da *pRequest* conterá o tamanho real do buffer.</span><span class="sxs-lookup"><span data-stu-id="f5cff-121">When the method returns, if the return value is S\_OK, the **cbBuffer** member of *pRequest* contains the actual buffer size.</span></span> <span data-ttu-id="f5cff-122">Isso pode ser maior que o tamanho solicitado, mas nunca será menor.</span><span class="sxs-lookup"><span data-stu-id="f5cff-122">This might be larger than the requested size, but will never be smaller.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5cff-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5cff-123">Requirements</span></span>



| <span data-ttu-id="f5cff-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5cff-124">Requirement</span></span> | <span data-ttu-id="f5cff-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f5cff-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5cff-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5cff-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f5cff-127"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5cff-127"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f5cff-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f5cff-128">Library</span></span><br/> | <dl> <span data-ttu-id="f5cff-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f5cff-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5cff-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5cff-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5cff-131">**Classe CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="f5cff-131">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




