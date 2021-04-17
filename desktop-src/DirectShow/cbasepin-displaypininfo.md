---
description: O método DisplayPinInfo rastreia uma conexão de PIN durante a depuração.
ms.assetid: 3c1aa5ab-7f6b-4518-abf3-b5138f6267ee
title: Método CBasePin. DisplayPinInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea563ca07eaea6b6974a831726918866414a33b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787422"
---
# <a name="cbasepindisplaypininfo-method"></a><span data-ttu-id="31749-103">Método CBasePin. DisplayPinInfo</span><span class="sxs-lookup"><span data-stu-id="31749-103">CBasePin.DisplayPinInfo method</span></span>

<span data-ttu-id="31749-104">O `DisplayPinInfo` método rastreia uma conexão de PIN durante a depuração.</span><span class="sxs-lookup"><span data-stu-id="31749-104">The `DisplayPinInfo` method traces a pin connection during debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="31749-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31749-105">Syntax</span></span>


```C++
void DisplayPinInfo(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="31749-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31749-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31749-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="31749-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="31749-108">Ponteiro para o pino de recebimento.</span><span class="sxs-lookup"><span data-stu-id="31749-108">Pointer to the receiving pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31749-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31749-109">Return value</span></span>

<span data-ttu-id="31749-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="31749-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="31749-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="31749-111">Remarks</span></span>

<span data-ttu-id="31749-112">Em compilações de depuração, esse método chama a função [**DbgLog**](dbglog.md) para rastrear uma tentativa de conexão.</span><span class="sxs-lookup"><span data-stu-id="31749-112">In debug builds, this method calls the [**DbgLog**](dbglog.md) function to trace a connection attempt.</span></span> <span data-ttu-id="31749-113">Em compilações de varejo, esse método não faz nada.</span><span class="sxs-lookup"><span data-stu-id="31749-113">In retail builds, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="31749-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31749-114">Requirements</span></span>



| <span data-ttu-id="31749-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="31749-115">Requirement</span></span> | <span data-ttu-id="31749-116">Valor</span><span class="sxs-lookup"><span data-stu-id="31749-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31749-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31749-117">Header</span></span><br/>  | <dl> <span data-ttu-id="31749-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31749-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="31749-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31749-119">Library</span></span><br/> | <dl> <span data-ttu-id="31749-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="31749-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31749-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="31749-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31749-122">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="31749-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




