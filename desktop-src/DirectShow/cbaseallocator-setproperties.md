---
description: 'O método SetProperties especifica o número de buffers a serem alocados e o tamanho de cada buffer. Esse método implementa o método IMemAllocator:: SetProperties.'
ms.assetid: f53c22a4-c01d-4d2f-81f0-bedf8f2ae5f0
title: Método CBaseAllocator. SetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 000da3ee359ad727e3af972fc4aa6d0dbbb9133e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812995"
---
# <a name="cbaseallocatorsetproperties-method"></a><span data-ttu-id="80758-104">Método CBaseAllocator. SetProperties</span><span class="sxs-lookup"><span data-stu-id="80758-104">CBaseAllocator.SetProperties method</span></span>

<span data-ttu-id="80758-105">O `SetProperties` método especifica o número de buffers a serem alocados e o tamanho de cada buffer.</span><span class="sxs-lookup"><span data-stu-id="80758-105">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span> <span data-ttu-id="80758-106">Esse método implementa o método [**IMemAllocator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) .</span><span class="sxs-lookup"><span data-stu-id="80758-106">This method implements the [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="80758-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80758-107">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="80758-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80758-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80758-109">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="80758-109">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="80758-110">Ponteiro para uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contém os requisitos de buffer.</span><span class="sxs-lookup"><span data-stu-id="80758-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="80758-111">*pActual*</span><span class="sxs-lookup"><span data-stu-id="80758-111">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="80758-112">Ponteiro para uma estrutura de **\_ Propriedades de alocador** que recebe as propriedades reais do buffer.</span><span class="sxs-lookup"><span data-stu-id="80758-112">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80758-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="80758-113">Return value</span></span>

<span data-ttu-id="80758-114">Retorna um dos valores de **HRESULT** a seguir.</span><span class="sxs-lookup"><span data-stu-id="80758-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="80758-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="80758-115">Return code</span></span>                                                                                                 | <span data-ttu-id="80758-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="80758-116">Description</span></span>                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="80758-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="80758-117"><dt>**S\_OK**</dt></span></span> </dl>                        | <span data-ttu-id="80758-118">Êxito.</span><span class="sxs-lookup"><span data-stu-id="80758-118">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="80758-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="80758-119"><dt>**E\_POINTER**</dt></span></span> </dl>                   | <span data-ttu-id="80758-120">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="80758-120">**NULL** pointer argument.</span></span><br/>                                 |
| <dl> <span data-ttu-id="80758-121"><dt>**VFW \_ E \_ já \_ confirmado**</dt></span><span class="sxs-lookup"><span data-stu-id="80758-121"><dt>**VFW\_E\_ALREADY\_COMMITTED**</dt></span></span> </dl>   | <span data-ttu-id="80758-122">Não é possível alterar a memória alocada enquanto o filtro estiver ativo.</span><span class="sxs-lookup"><span data-stu-id="80758-122">Cannot change allocated memory while the filter is active.</span></span><br/> |
| <dl> <span data-ttu-id="80758-123"><dt>**VFW \_ E \_ BADALIGN**</dt></span><span class="sxs-lookup"><span data-stu-id="80758-123"><dt>**VFW\_E\_BADALIGN**</dt></span></span> </dl>             | <span data-ttu-id="80758-124">Foi especificado um alinhamento inválido.</span><span class="sxs-lookup"><span data-stu-id="80758-124">An invalid alignment was specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="80758-125"><dt>**VFW \_ E \_ buffers \_ pendentes**</dt></span><span class="sxs-lookup"><span data-stu-id="80758-125"><dt>**VFW\_E\_BUFFERS\_OUTSTANDING**</dt></span></span> </dl> | <span data-ttu-id="80758-126">Um ou mais buffers ainda estão ativos.</span><span class="sxs-lookup"><span data-stu-id="80758-126">One or more buffers are still active.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="80758-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="80758-127">Remarks</span></span>

<span data-ttu-id="80758-128">Esse método especifica os requisitos de buffer, mas não aloca nenhum buffer.</span><span class="sxs-lookup"><span data-stu-id="80758-128">This method specifies the buffer requirements, but does not allocate any buffers.</span></span> <span data-ttu-id="80758-129">Chame o método [**CBaseAllocator:: Commit**](cbaseallocator-commit.md) para alocar buffers.</span><span class="sxs-lookup"><span data-stu-id="80758-129">Call the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method to allocate buffers.</span></span>

<span data-ttu-id="80758-130">O chamador aloca duas estruturas de propriedades de ALOCAdor \_ .</span><span class="sxs-lookup"><span data-stu-id="80758-130">The caller allocates two ALLOCATOR\_PROPERTIES structures.</span></span> <span data-ttu-id="80758-131">O parâmetro de *pRequest* contém os requisitos de buffer do chamador, incluindo o número de buffers e o tamanho de cada buffer.</span><span class="sxs-lookup"><span data-stu-id="80758-131">The *pRequest* parameter contains the caller's buffer requirements, including the number of buffers and the size of each buffer.</span></span> <span data-ttu-id="80758-132">Quando o método retorna, o parâmetro *Pactual* contém as propriedades de buffer reais, conforme definido pelo alocador.</span><span class="sxs-lookup"><span data-stu-id="80758-132">When the method returns, the *pActual* parameter contains the actual buffer properties, as set by the allocator.</span></span> <span data-ttu-id="80758-133">Na classe base, supondo que o método tenha sucesso, as propriedades reais sempre correspondem às propriedades solicitadas.</span><span class="sxs-lookup"><span data-stu-id="80758-133">In the base class, assuming that the method succeeds, the actual properties always match the requested properties.</span></span> <span data-ttu-id="80758-134">Classes derivadas podem substituir esse comportamento.</span><span class="sxs-lookup"><span data-stu-id="80758-134">Derived classes might override this behavior.</span></span>

<span data-ttu-id="80758-135">O alocador não deve ser confirmado e não deve ter buffers pendentes.</span><span class="sxs-lookup"><span data-stu-id="80758-135">The allocator must not be committed, and must not have outstanding buffers.</span></span> <span data-ttu-id="80758-136">Na classe base, o alinhamento deve ser igual a 1.</span><span class="sxs-lookup"><span data-stu-id="80758-136">In the base class, the alignment must equal 1.</span></span> <span data-ttu-id="80758-137">A classe [**CMemAllocator**](cmemallocator.md) substitui esse requisito.</span><span class="sxs-lookup"><span data-stu-id="80758-137">The [**CMemAllocator**](cmemallocator.md) class overrides this requirement.</span></span>

## <a name="requirements"></a><span data-ttu-id="80758-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80758-138">Requirements</span></span>



| <span data-ttu-id="80758-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="80758-139">Requirement</span></span> | <span data-ttu-id="80758-140">Valor</span><span class="sxs-lookup"><span data-stu-id="80758-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80758-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="80758-141">Header</span></span><br/>  | <dl> <span data-ttu-id="80758-142"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80758-142"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="80758-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80758-143">Library</span></span><br/> | <dl> <span data-ttu-id="80758-144"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="80758-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80758-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="80758-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80758-146">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="80758-146">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




