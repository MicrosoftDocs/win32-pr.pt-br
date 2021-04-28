---
description: Construtor de CSystemClock. CSystemClock-método de construtor.
ms.assetid: facc2c9d-034a-4fed-b6fe-77a40e36c305
title: Construtor CSystemClock. CSystemClock (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CSystemClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 11ba7449b086f84dc2caff19da922c03f9c7103b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095194"
---
# <a name="csystemclockcsystemclock-constructor"></a><span data-ttu-id="6d8d4-103">Construtor CSystemClock. CSystemClock</span><span class="sxs-lookup"><span data-stu-id="6d8d4-103">CSystemClock.CSystemClock constructor</span></span>

<span data-ttu-id="6d8d4-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="6d8d4-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d8d4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d8d4-105">Syntax</span></span>


```C++
CSystemClock(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="6d8d4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d8d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d8d4-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="6d8d4-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="6d8d4-108">Cadeia de caracteres que contém o nome de depuração do objeto.</span><span class="sxs-lookup"><span data-stu-id="6d8d4-108">String containing the debug name of the object.</span></span> <span data-ttu-id="6d8d4-109">Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="6d8d4-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d8d4-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="6d8d4-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="6d8d4-111">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="6d8d4-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="6d8d4-112">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="6d8d4-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="6d8d4-113">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6d8d4-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6d8d4-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="6d8d4-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="6d8d4-115">Ponteiro para o valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6d8d4-115">Pointer to the **HRESULT** value.</span></span> <span data-ttu-id="6d8d4-116">Se ocorrer um erro, o método retornará um código de erro nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6d8d4-116">If an error occurs, the method returns an error code in this parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d8d4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d8d4-117">Requirements</span></span>



| <span data-ttu-id="6d8d4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d8d4-118">Requirement</span></span> | <span data-ttu-id="6d8d4-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6d8d4-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d8d4-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d8d4-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6d8d4-121"><dt>Sysclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d8d4-121"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6d8d4-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d8d4-122">Library</span></span><br/> | <dl> <span data-ttu-id="6d8d4-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6d8d4-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




