---
description: A função EqualPins verifica se dois Pins estão no mesmo objeto.
ms.assetid: b6a92cb6-f4a9-4a14-831c-3b123e4692c0
title: Função EqualPins (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EqualPins
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fdf499b494f41a0acc5cc446bc92deade61c045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782849"
---
# <a name="equalpins-function"></a><span data-ttu-id="0a7d1-103">Função EqualPins</span><span class="sxs-lookup"><span data-stu-id="0a7d1-103">EqualPins function</span></span>

<span data-ttu-id="0a7d1-104">A função EqualPins verifica se dois Pins estão no mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="0a7d1-104">The EqualPins function checks if two pins are on the same object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a7d1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a7d1-105">Syntax</span></span>


```C++
BOOL EqualPins(
   IUnknown *pPin1,
   IUnknown *pPin2
);
```



## <a name="parameters"></a><span data-ttu-id="0a7d1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a7d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a7d1-107">*pPin1*</span><span class="sxs-lookup"><span data-stu-id="0a7d1-107">*pPin1*</span></span> 
</dt> <dd>

<span data-ttu-id="0a7d1-108">Ponteiro para um PIN.</span><span class="sxs-lookup"><span data-stu-id="0a7d1-108">Pointer to one pin.</span></span>

</dd> <dt>

<span data-ttu-id="0a7d1-109">*pPin2*</span><span class="sxs-lookup"><span data-stu-id="0a7d1-109">*pPin2*</span></span> 
</dt> <dd>

<span data-ttu-id="0a7d1-110">Ponteiro para o outro PIN.</span><span class="sxs-lookup"><span data-stu-id="0a7d1-110">Pointer to the other pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a7d1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0a7d1-111">Return value</span></span>

<span data-ttu-id="0a7d1-112">Retornará **true** se ambos os Pins estiverem no mesmo objeto ou **false** .</span><span class="sxs-lookup"><span data-stu-id="0a7d1-112">Returns **TRUE** if both pins are on the same object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a7d1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a7d1-113">Requirements</span></span>



| <span data-ttu-id="0a7d1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a7d1-114">Requirement</span></span> | <span data-ttu-id="0a7d1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0a7d1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a7d1-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0a7d1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0a7d1-117"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a7d1-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0a7d1-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0a7d1-118">Library</span></span><br/> | <dl> <span data-ttu-id="0a7d1-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0a7d1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a7d1-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a7d1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a7d1-121">Funções auxiliares diversas</span><span class="sxs-lookup"><span data-stu-id="0a7d1-121">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




