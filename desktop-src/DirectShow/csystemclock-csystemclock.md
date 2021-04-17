---
description: Método de construtor.
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
ms.openlocfilehash: fea99d95aa4c1b1cadefbb95384fb871374362f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747811"
---
# <a name="csystemclockcsystemclock-constructor"></a><span data-ttu-id="d372f-103">Construtor CSystemClock. CSystemClock</span><span class="sxs-lookup"><span data-stu-id="d372f-103">CSystemClock.CSystemClock constructor</span></span>

<span data-ttu-id="d372f-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="d372f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d372f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d372f-105">Syntax</span></span>


```C++
CSystemClock(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="d372f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d372f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d372f-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="d372f-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="d372f-108">Cadeia de caracteres que contém o nome de depuração do objeto.</span><span class="sxs-lookup"><span data-stu-id="d372f-108">String containing the debug name of the object.</span></span> <span data-ttu-id="d372f-109">Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="d372f-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="d372f-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="d372f-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="d372f-111">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="d372f-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="d372f-112">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="d372f-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="d372f-113">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d372f-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d372f-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="d372f-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d372f-115">Ponteiro para o valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d372f-115">Pointer to the **HRESULT** value.</span></span> <span data-ttu-id="d372f-116">Se ocorrer um erro, o método retornará um código de erro nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d372f-116">If an error occurs, the method returns an error code in this parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d372f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d372f-117">Requirements</span></span>



| <span data-ttu-id="d372f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d372f-118">Requirement</span></span> | <span data-ttu-id="d372f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d372f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d372f-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d372f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d372f-121"><dt>Sysclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d372f-121"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d372f-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d372f-122">Library</span></span><br/> | <dl> <span data-ttu-id="d372f-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d372f-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




