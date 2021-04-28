---
description: Construtor de CMemAllocator. CMemAllocator-método de construtor.
ms.assetid: 2340b39a-cab6-4524-b8cd-b22d4bdd24d0
title: Construtor CMemAllocator. CMemAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1151572c32efe69cceb89e7a5ea5a045955b5f43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095394"
---
# <a name="cmemallocatorcmemallocator-constructor"></a><span data-ttu-id="66309-103">Construtor CMemAllocator. CMemAllocator</span><span class="sxs-lookup"><span data-stu-id="66309-103">CMemAllocator.CMemAllocator constructor</span></span>

<span data-ttu-id="66309-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="66309-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="66309-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66309-105">Syntax</span></span>


```C++
CMemAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="66309-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66309-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66309-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="66309-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="66309-108">Ponteiro para uma cadeia de caracteres que contém o nome do alocador.</span><span class="sxs-lookup"><span data-stu-id="66309-108">Pointer to a string containing the name of the allocator.</span></span>

</dd> <dt>

<span data-ttu-id="66309-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="66309-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="66309-110">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="66309-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="66309-111">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="66309-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="66309-112">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="66309-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="66309-113">*phr*</span><span class="sxs-lookup"><span data-stu-id="66309-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="66309-114">Ponteiro para uma variável que recebe um valor **HRESULT** que indica o êxito ou a falha do método.</span><span class="sxs-lookup"><span data-stu-id="66309-114">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66309-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66309-115">Requirements</span></span>



| <span data-ttu-id="66309-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="66309-116">Requirement</span></span> | <span data-ttu-id="66309-117">Valor</span><span class="sxs-lookup"><span data-stu-id="66309-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66309-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66309-118">Header</span></span><br/>  | <dl> <span data-ttu-id="66309-119"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66309-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="66309-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66309-120">Library</span></span><br/> | <dl> <span data-ttu-id="66309-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="66309-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66309-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="66309-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66309-123">**Classe CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="66309-123">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




