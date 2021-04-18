---
description: O método SetProperties especifica o número de buffers a serem alocados e o tamanho de cada buffer.
ms.assetid: 01f63379-1d66-4a72-b87c-de55504b0bb4
title: Método CMemAllocator. SetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8505916245cca81fdd84132e4523fe9dd03b971b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778497"
---
# <a name="cmemallocatorsetproperties-method"></a><span data-ttu-id="38c1c-103">Método CMemAllocator. SetProperties</span><span class="sxs-lookup"><span data-stu-id="38c1c-103">CMemAllocator.SetProperties method</span></span>

<span data-ttu-id="38c1c-104">O `SetProperties` método especifica o número de buffers a serem alocados e o tamanho de cada buffer.</span><span class="sxs-lookup"><span data-stu-id="38c1c-104">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="38c1c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38c1c-105">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="38c1c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38c1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38c1c-107">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="38c1c-107">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="38c1c-108">Ponteiro para uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contém os requisitos de buffer.</span><span class="sxs-lookup"><span data-stu-id="38c1c-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="38c1c-109">*pActual*</span><span class="sxs-lookup"><span data-stu-id="38c1c-109">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="38c1c-110">Ponteiro para uma estrutura de **\_ Propriedades de alocador** que recebe as propriedades reais do buffer.</span><span class="sxs-lookup"><span data-stu-id="38c1c-110">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38c1c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38c1c-111">Return value</span></span>

<span data-ttu-id="38c1c-112">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="38c1c-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="38c1c-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="38c1c-113">Return code</span></span>                                                                                                 | <span data-ttu-id="38c1c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="38c1c-114">Description</span></span>                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="38c1c-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="38c1c-115"><dt>**S\_OK**</dt></span></span> </dl>                        | <span data-ttu-id="38c1c-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="38c1c-116">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="38c1c-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="38c1c-117"><dt>**E\_POINTER**</dt></span></span> </dl>                   | <span data-ttu-id="38c1c-118">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="38c1c-118">**NULL** pointer argument.</span></span><br/>                                 |
| <dl> <span data-ttu-id="38c1c-119"><dt>**VFW \_ E \_ já \_ confirmado**</dt></span><span class="sxs-lookup"><span data-stu-id="38c1c-119"><dt>**VFW\_E\_ALREADY\_COMMITTED**</dt></span></span> </dl>   | <span data-ttu-id="38c1c-120">Não é possível alterar a memória alocada enquanto o filtro estiver ativo.</span><span class="sxs-lookup"><span data-stu-id="38c1c-120">Cannot change allocated memory while the filter is active.</span></span><br/> |
| <dl> <span data-ttu-id="38c1c-121"><dt>**VFW \_ E \_ BADALIGN**</dt></span><span class="sxs-lookup"><span data-stu-id="38c1c-121"><dt>**VFW\_E\_BADALIGN**</dt></span></span> </dl>             | <span data-ttu-id="38c1c-122">Foi especificado um alinhamento inválido.</span><span class="sxs-lookup"><span data-stu-id="38c1c-122">An invalid alignment was specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="38c1c-123"><dt>**VFW \_ E \_ buffers \_ pendentes**</dt></span><span class="sxs-lookup"><span data-stu-id="38c1c-123"><dt>**VFW\_E\_BUFFERS\_OUTSTANDING**</dt></span></span> </dl> | <span data-ttu-id="38c1c-124">Um ou mais buffers ainda estão ativos.</span><span class="sxs-lookup"><span data-stu-id="38c1c-124">One or more buffers are still active.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="38c1c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="38c1c-125">Remarks</span></span>

<span data-ttu-id="38c1c-126">Esse método substitui o método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="38c1c-126">This method overrides the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method.</span></span>

<span data-ttu-id="38c1c-127">O alinhamento do buffer, especificado pelo membro **cbAlign** da estrutura **de \_ Propriedades do alocador** , deve ser uma potência par de dois.</span><span class="sxs-lookup"><span data-stu-id="38c1c-127">The buffer alignment, specified by the **cbAlign** member of the **ALLOCATOR\_PROPERTIES** structure, must be an even power of two.</span></span>

## <a name="requirements"></a><span data-ttu-id="38c1c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38c1c-128">Requirements</span></span>



| <span data-ttu-id="38c1c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="38c1c-129">Requirement</span></span> | <span data-ttu-id="38c1c-130">Valor</span><span class="sxs-lookup"><span data-stu-id="38c1c-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38c1c-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38c1c-131">Header</span></span><br/>  | <dl> <span data-ttu-id="38c1c-132"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38c1c-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="38c1c-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38c1c-133">Library</span></span><br/> | <dl> <span data-ttu-id="38c1c-134"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="38c1c-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38c1c-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="38c1c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38c1c-136">**Classe CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="38c1c-136">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




