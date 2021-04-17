---
description: O método AlignDown Trunca um valor para um limite de alinhamento especificado.
ms.assetid: f0efdedb-67ec-49d6-92a8-54485aa04e15
title: Método CPullPin. AlignDown (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignDown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1383517f4931fa153fd141878475cc8775a61045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789700"
---
# <a name="cpullpinaligndown-method"></a><span data-ttu-id="0be7d-103">Método CPullPin. AlignDown</span><span class="sxs-lookup"><span data-stu-id="0be7d-103">CPullPin.AlignDown method</span></span>

<span data-ttu-id="0be7d-104">O `AlignDown` método Trunca um valor para um limite de alinhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="0be7d-104">The `AlignDown` method truncates a value to a specified alignment boundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="0be7d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0be7d-105">Syntax</span></span>


```C++
LONGLONG AlignDown(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a><span data-ttu-id="0be7d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0be7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0be7d-107">*precisa*</span><span class="sxs-lookup"><span data-stu-id="0be7d-107">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="0be7d-108">Especifica o número a ser alinhado.</span><span class="sxs-lookup"><span data-stu-id="0be7d-108">Specifies the number to align.</span></span>

</dd> <dt>

<span data-ttu-id="0be7d-109">*lAlign*</span><span class="sxs-lookup"><span data-stu-id="0be7d-109">*lAlign*</span></span> 
</dt> <dd>

<span data-ttu-id="0be7d-110">Especifica o limite de alinhamento.</span><span class="sxs-lookup"><span data-stu-id="0be7d-110">Specifies the alignment boundary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0be7d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0be7d-111">Return value</span></span>

<span data-ttu-id="0be7d-112">Retorna o resultado alinhado.</span><span class="sxs-lookup"><span data-stu-id="0be7d-112">Returns the aligned result.</span></span>

## <a name="requirements"></a><span data-ttu-id="0be7d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0be7d-113">Requirements</span></span>



| <span data-ttu-id="0be7d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0be7d-114">Requirement</span></span> | <span data-ttu-id="0be7d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0be7d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0be7d-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0be7d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0be7d-117"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="0be7d-117"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="0be7d-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0be7d-118">Library</span></span><br/> | <dl> <span data-ttu-id="0be7d-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0be7d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0be7d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="0be7d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0be7d-121">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="0be7d-121">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




