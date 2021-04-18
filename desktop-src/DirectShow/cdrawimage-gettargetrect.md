---
description: O método GetTargetRect recupera o retângulo de destino atual.
ms.assetid: b6542b06-af36-4666-b6fa-d9fa3c6c7044
title: Método CDrawImage. GetTargetRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 547dd12117cec95ad1cb0159667a8dd72a95a6e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810255"
---
# <a name="cdrawimagegettargetrect-method"></a><span data-ttu-id="330a7-103">Método CDrawImage. GetTargetRect</span><span class="sxs-lookup"><span data-stu-id="330a7-103">CDrawImage.GetTargetRect method</span></span>

<span data-ttu-id="330a7-104">O `GetTargetRect` método recupera o retângulo de destino atual.</span><span class="sxs-lookup"><span data-stu-id="330a7-104">The `GetTargetRect` method retrieves the current destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="330a7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="330a7-105">Syntax</span></span>


```C++
void GetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a><span data-ttu-id="330a7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="330a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="330a7-107">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="330a7-107">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="330a7-108">Ponteiro para uma estrutura **Rect** que recebe o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="330a7-108">Pointer to a **RECT** structure that receives the target rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="330a7-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="330a7-109">Return value</span></span>

<span data-ttu-id="330a7-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="330a7-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="330a7-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="330a7-111">Requirements</span></span>



| <span data-ttu-id="330a7-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="330a7-112">Requirement</span></span> | <span data-ttu-id="330a7-113">Valor</span><span class="sxs-lookup"><span data-stu-id="330a7-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="330a7-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="330a7-114">Header</span></span><br/>  | <dl> <span data-ttu-id="330a7-115"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="330a7-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="330a7-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="330a7-116">Library</span></span><br/> | <dl> <span data-ttu-id="330a7-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="330a7-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="330a7-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="330a7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="330a7-119">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="330a7-119">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




