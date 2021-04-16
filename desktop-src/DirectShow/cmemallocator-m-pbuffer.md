---
description: Ponteiro para o bloco de memória que contém os buffers.
ms.assetid: b9d08f5b-8616-4f68-869a-e8ebb77ccdc1
title: 'Membro CMemAllocator:: m_pBuffer (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pBuffer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ae988474196e323cde24305b0e389ac69f0f10d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758544"
---
# <a name="cmemallocatorm_pbuffer-member"></a><span data-ttu-id="59749-103">Membro de CMemAllocator:: m \_ pBuffer</span><span class="sxs-lookup"><span data-stu-id="59749-103">CMemAllocator::m\_pBuffer member</span></span>

<span data-ttu-id="59749-104">Ponteiro para o bloco de memória que contém os buffers.</span><span class="sxs-lookup"><span data-stu-id="59749-104">Pointer to the memory block that contains the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="59749-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59749-105">Syntax</span></span>


```C++
LPBYTE m_pBuffer;
```



## <a name="remarks"></a><span data-ttu-id="59749-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="59749-106">Remarks</span></span>

<span data-ttu-id="59749-107">Os buffers de exemplo são calculados como deslocamentos desse ponteiro.</span><span class="sxs-lookup"><span data-stu-id="59749-107">Sample buffers are calculated as offsets from this pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="59749-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59749-108">Requirements</span></span>



| <span data-ttu-id="59749-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="59749-109">Requirement</span></span> | <span data-ttu-id="59749-110">Valor</span><span class="sxs-lookup"><span data-stu-id="59749-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59749-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59749-111">Header</span></span><br/>  | <dl> <span data-ttu-id="59749-112"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59749-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="59749-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59749-113">Library</span></span><br/> | <dl> <span data-ttu-id="59749-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="59749-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59749-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="59749-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59749-116">**Classe CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="59749-116">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




