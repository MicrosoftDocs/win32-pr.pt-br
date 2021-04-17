---
description: O método GetSourceRect recupera o retângulo de origem atual.
ms.assetid: e9ca091f-3fd7-4e42-90e9-b7831dd488a9
title: Método CDrawImage. GetSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a2188a183794b94a5d6d05ac237f91dbcb5d6dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787411"
---
# <a name="cdrawimagegetsourcerect-method"></a><span data-ttu-id="c03db-103">Método CDrawImage. GetSourceRect</span><span class="sxs-lookup"><span data-stu-id="c03db-103">CDrawImage.GetSourceRect method</span></span>

<span data-ttu-id="c03db-104">O `GetSourceRect` método recupera o retângulo de origem atual.</span><span class="sxs-lookup"><span data-stu-id="c03db-104">The `GetSourceRect` method retrieves the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="c03db-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c03db-105">Syntax</span></span>


```C++
void GetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="c03db-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c03db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c03db-107">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="c03db-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="c03db-108">Ponteiro para uma estrutura **Rect** que recebe o retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="c03db-108">Pointer to a **RECT** structure that receives the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c03db-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c03db-109">Return value</span></span>

<span data-ttu-id="c03db-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c03db-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c03db-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c03db-111">Requirements</span></span>



| <span data-ttu-id="c03db-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c03db-112">Requirement</span></span> | <span data-ttu-id="c03db-113">Valor</span><span class="sxs-lookup"><span data-stu-id="c03db-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c03db-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c03db-114">Header</span></span><br/>  | <dl> <span data-ttu-id="c03db-115"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c03db-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c03db-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c03db-116">Library</span></span><br/> | <dl> <span data-ttu-id="c03db-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c03db-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c03db-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="c03db-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c03db-119">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="c03db-119">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




