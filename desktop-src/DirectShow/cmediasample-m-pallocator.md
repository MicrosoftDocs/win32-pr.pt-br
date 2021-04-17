---
description: Ponteiro para o alocador que criou este exemplo.
ms.assetid: b4faccec-9124-4ae6-8662-ac5eb017328a
title: 'Membro CMediaSample:: m_pAllocator (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac2943c08b881badd8e15ea0633952ccc973a534
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769228"
---
# <a name="cmediasamplem_pallocator-member"></a><span data-ttu-id="58bc6-103">Membro de CMediaSample:: m \_ pAllocator</span><span class="sxs-lookup"><span data-stu-id="58bc6-103">CMediaSample::m\_pAllocator member</span></span>

<span data-ttu-id="58bc6-104">Ponteiro para o alocador que criou este exemplo.</span><span class="sxs-lookup"><span data-stu-id="58bc6-104">Pointer to the allocator that created this sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="58bc6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58bc6-105">Syntax</span></span>


```C++
CBaseAllocator *m_pAllocator;
```



## <a name="remarks"></a><span data-ttu-id="58bc6-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="58bc6-106">Remarks</span></span>

<span data-ttu-id="58bc6-107">Embora o exemplo mantenha um ponteiro para o alocador, ele não mantém uma contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="58bc6-107">Although the sample keeps a pointer to the allocator, it does not hold a reference count.</span></span> <span data-ttu-id="58bc6-108">Em vez disso, o alocador incrementa sua própria contagem de referência no método [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) e se libera no método [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="58bc6-108">Instead, the allocator increments its own reference count in the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method, and releases itself in the [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method.</span></span> <span data-ttu-id="58bc6-109">Isso garante que o alocador estará disponível desde que outro objeto esteja usando o exemplo.</span><span class="sxs-lookup"><span data-stu-id="58bc6-109">This guarantees that the allocator will be available as long as another object is using the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="58bc6-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58bc6-110">Requirements</span></span>



| <span data-ttu-id="58bc6-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="58bc6-111">Requirement</span></span> | <span data-ttu-id="58bc6-112">Valor</span><span class="sxs-lookup"><span data-stu-id="58bc6-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58bc6-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="58bc6-113">Header</span></span><br/>  | <dl> <span data-ttu-id="58bc6-114"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58bc6-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="58bc6-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58bc6-115">Library</span></span><br/> | <dl> <span data-ttu-id="58bc6-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="58bc6-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58bc6-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="58bc6-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58bc6-118">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="58bc6-118">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




