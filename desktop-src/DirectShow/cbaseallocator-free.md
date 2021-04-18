---
description: O método gratuito libera toda a memória do buffer. Esse método é chamado quando o filtro proprietário deconfirma o alocador, após o lançamento da última amostra de mídia.
ms.assetid: dd1e6c4d-762a-4caf-902b-015c6c9fdb4d
title: Método CBaseAllocator. Free (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3534eac01a6769e090c8c808f16cc6ad5c6b84c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770304"
---
# <a name="cbaseallocatorfree-method"></a><span data-ttu-id="88ab6-104">Método CBaseAllocator. Free</span><span class="sxs-lookup"><span data-stu-id="88ab6-104">CBaseAllocator.Free method</span></span>

<span data-ttu-id="88ab6-105">O `Free` método libera toda a memória do buffer.</span><span class="sxs-lookup"><span data-stu-id="88ab6-105">The `Free` method releases all of the buffer memory.</span></span> <span data-ttu-id="88ab6-106">Esse método é chamado quando o filtro proprietário deconfirma o alocador, após o lançamento da última amostra de mídia.</span><span class="sxs-lookup"><span data-stu-id="88ab6-106">This method is called when the owning filter decommits the allocator, after the last media sample is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="88ab6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88ab6-107">Syntax</span></span>


```C++
virtual void Free() = 0;
```



## <a name="parameters"></a><span data-ttu-id="88ab6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88ab6-108">Parameters</span></span>

<span data-ttu-id="88ab6-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="88ab6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88ab6-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="88ab6-110">Return value</span></span>

<span data-ttu-id="88ab6-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="88ab6-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88ab6-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="88ab6-112">Remarks</span></span>

<span data-ttu-id="88ab6-113">Depois que o método [**decommit**](cbaseallocator-decommit.md) é chamado, o alocador chama esse método quando libera o último exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="88ab6-113">After the [**Decommit**](cbaseallocator-decommit.md) method is called, the allocator calls this method when it releases the last media sample.</span></span> <span data-ttu-id="88ab6-114">A classe derivada deve implementar esse método.</span><span class="sxs-lookup"><span data-stu-id="88ab6-114">The derived class must implement this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="88ab6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88ab6-115">Requirements</span></span>



| <span data-ttu-id="88ab6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="88ab6-116">Requirement</span></span> | <span data-ttu-id="88ab6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="88ab6-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88ab6-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="88ab6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="88ab6-119"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88ab6-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="88ab6-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="88ab6-120">Library</span></span><br/> | <dl> <span data-ttu-id="88ab6-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="88ab6-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88ab6-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="88ab6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ab6-123">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="88ab6-123">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




