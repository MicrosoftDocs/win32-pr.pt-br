---
description: O método GetFreeCount recupera o número de amostras de mídia que não estão em uso.
ms.assetid: f4ce4cca-0168-42db-9fe7-858862f033a8
title: Método CBaseAllocator. GetFreeCount (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetFreeCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0538229053b5d47ca1bdc8f30b38a0937e36cb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780895"
---
# <a name="cbaseallocatorgetfreecount-method"></a><span data-ttu-id="af87f-103">Método CBaseAllocator. GetFreeCount</span><span class="sxs-lookup"><span data-stu-id="af87f-103">CBaseAllocator.GetFreeCount method</span></span>

<span data-ttu-id="af87f-104">O `GetFreeCount` método recupera o número de amostras de mídia que não estão em uso.</span><span class="sxs-lookup"><span data-stu-id="af87f-104">The `GetFreeCount` method retrieves the number of media samples that are not in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="af87f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af87f-105">Syntax</span></span>


```C++
HRESULT GetFreeCount(
   LONG *plBuffersFree
);
```



## <a name="parameters"></a><span data-ttu-id="af87f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af87f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af87f-107">*plBuffersFree*</span><span class="sxs-lookup"><span data-stu-id="af87f-107">*plBuffersFree*</span></span> 
</dt> <dd>

<span data-ttu-id="af87f-108">Endereço de uma variável que recebe o número de amostras que não estão em uso.</span><span class="sxs-lookup"><span data-stu-id="af87f-108">Address of a variable that receives the number of samples that are not in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af87f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af87f-109">Return value</span></span>

<span data-ttu-id="af87f-110">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="af87f-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="af87f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="af87f-111">Remarks</span></span>

<span data-ttu-id="af87f-112">Esse método implementa o método [**IMemAllocatorCallbackTemp:: GetFreeCount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) .</span><span class="sxs-lookup"><span data-stu-id="af87f-112">This method implements the [**IMemAllocatorCallbackTemp::GetFreeCount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) method.</span></span> <span data-ttu-id="af87f-113">O alocador não expõe a interface IMemAllocatorCallbackTemp, a menos que o sinalizador *fEnableReleaseCallback* seja definido como **true** no Construtor CBaseAllocator.</span><span class="sxs-lookup"><span data-stu-id="af87f-113">The allocator does not expose the IMemAllocatorCallbackTemp interface unless the *fEnableReleaseCallback* flag is set to **TRUE** in the CBaseAllocator constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="af87f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af87f-114">Requirements</span></span>



| <span data-ttu-id="af87f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="af87f-115">Requirement</span></span> | <span data-ttu-id="af87f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="af87f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af87f-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af87f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="af87f-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af87f-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="af87f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af87f-119">Library</span></span><br/> | <dl> <span data-ttu-id="af87f-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="af87f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af87f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="af87f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af87f-122">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="af87f-122">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




