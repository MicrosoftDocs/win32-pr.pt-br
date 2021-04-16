---
description: O método CreateInstance cria uma nova instância da classe CMemAllocator.
ms.assetid: 87a831a4-2414-4240-8448-c5d90f130470
title: Método CMemAllocator. CreateInstance (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ef85de95db74e8a9d7aa6a7b1ba977620a29826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758853"
---
# <a name="cmemallocatorcreateinstance-method"></a><span data-ttu-id="768f2-103">Método CMemAllocator. CreateInstance</span><span class="sxs-lookup"><span data-stu-id="768f2-103">CMemAllocator.CreateInstance method</span></span>

<span data-ttu-id="768f2-104">O `CreateInstance` método cria uma nova instância da classe **CMemAllocator** .</span><span class="sxs-lookup"><span data-stu-id="768f2-104">The `CreateInstance` method creates a new instance of the **CMemAllocator** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="768f2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="768f2-105">Syntax</span></span>


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="768f2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="768f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="768f2-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="768f2-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="768f2-108">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="768f2-108">Pointer to the owner of this object.</span></span> <span data-ttu-id="768f2-109">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="768f2-109">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="768f2-110">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="768f2-110">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="768f2-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="768f2-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="768f2-112">Ponteiro para uma variável que recebe um valor **HRESULT** que indica o êxito ou a falha do método.</span><span class="sxs-lookup"><span data-stu-id="768f2-112">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="768f2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="768f2-113">Return value</span></span>

<span data-ttu-id="768f2-114">Retorna um ponteiro para um novo objeto **CMemAllocator** , tipado como um objeto **CUnknown** .</span><span class="sxs-lookup"><span data-stu-id="768f2-114">Returns a pointer to a new **CMemAllocator** object, typed as a **CUnknown** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="768f2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="768f2-115">Requirements</span></span>



| <span data-ttu-id="768f2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="768f2-116">Requirement</span></span> | <span data-ttu-id="768f2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="768f2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="768f2-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="768f2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="768f2-119"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="768f2-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="768f2-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="768f2-120">Library</span></span><br/> | <dl> <span data-ttu-id="768f2-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="768f2-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="768f2-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="768f2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="768f2-123">**Classe CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="768f2-123">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




