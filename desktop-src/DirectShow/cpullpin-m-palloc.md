---
description: A \_ variável de membro m pAlloc é um ponteiro para a interface IMemAllocator do alocador de memória.
ms.assetid: a3be5982-83f0-4552-9bcd-85da4a4918ff
title: 'Membro CPullPin:: m_pAlloc (Pullpin. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAlloc
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9945bd7b5f3c5b54f0ef578c2b012d0e56935d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750466"
---
# <a name="cpullpinm_palloc-member"></a><span data-ttu-id="74121-103">Membro de CPullPin:: m \_ pAlloc</span><span class="sxs-lookup"><span data-stu-id="74121-103">CPullPin::m\_pAlloc member</span></span>

<span data-ttu-id="74121-104">A `m_pAlloc` variável de membro é um ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador de memória.</span><span class="sxs-lookup"><span data-stu-id="74121-104">The `m_pAlloc` member variable is a pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="74121-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74121-105">Syntax</span></span>


```C++
IMemAllocator *m_pAlloc;
```



## <a name="remarks"></a><span data-ttu-id="74121-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="74121-106">Remarks</span></span>

<span data-ttu-id="74121-107">O método [**CPullPin::D ecideallocator**](cpullpin-decideallocator.md) define essa variável de membro.</span><span class="sxs-lookup"><span data-stu-id="74121-107">The [**CPullPin::DecideAllocator**](cpullpin-decideallocator.md) method sets this member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="74121-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74121-108">Requirements</span></span>



| <span data-ttu-id="74121-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="74121-109">Requirement</span></span> | <span data-ttu-id="74121-110">Valor</span><span class="sxs-lookup"><span data-stu-id="74121-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74121-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74121-111">Header</span></span><br/>  | <dl> <span data-ttu-id="74121-112"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="74121-112"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="74121-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74121-113">Library</span></span><br/> | <dl> <span data-ttu-id="74121-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="74121-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74121-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="74121-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74121-116">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="74121-116">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




