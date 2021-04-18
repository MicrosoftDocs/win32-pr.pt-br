---
description: O método CountSetBits retorna o número de bits definido como 1 em um campo de bit especificado.
ms.assetid: fc5701b8-88ff-4c23-9d26-854bb65cc55c
title: Método CImageDisplay. CountSetBits (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountSetBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb425b08b524b1d36b622bcfffcc9f311dccbbdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810252"
---
# <a name="cimagedisplaycountsetbits-method"></a><span data-ttu-id="e1390-103">Método CImageDisplay. CountSetBits</span><span class="sxs-lookup"><span data-stu-id="e1390-103">CImageDisplay.CountSetBits method</span></span>

<span data-ttu-id="e1390-104">O `CountSetBits` método retorna o número de bits definido como 1 em um campo de bit especificado.</span><span class="sxs-lookup"><span data-stu-id="e1390-104">The `CountSetBits` method returns the number of bits set to 1 in a specified bit field.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1390-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1390-105">Syntax</span></span>


```C++
DWORD CountSetBits(
   const DWORD Field
);
```



## <a name="parameters"></a><span data-ttu-id="e1390-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1390-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1390-107">*Campo*</span><span class="sxs-lookup"><span data-stu-id="e1390-107">*Field*</span></span> 
</dt> <dd>

<span data-ttu-id="e1390-108">Especifica um campo de bits como um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e1390-108">Specifies a bit field as a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1390-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1390-109">Return value</span></span>

<span data-ttu-id="e1390-110">Retorna o número de bits que são definidos como 1.</span><span class="sxs-lookup"><span data-stu-id="e1390-110">Returns the number of bits that are set to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1390-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1390-111">Requirements</span></span>



| <span data-ttu-id="e1390-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1390-112">Requirement</span></span> | <span data-ttu-id="e1390-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e1390-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1390-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e1390-114">Header</span></span><br/>  | <dl> <span data-ttu-id="e1390-115"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1390-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e1390-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1390-116">Library</span></span><br/> | <dl> <span data-ttu-id="e1390-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e1390-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1390-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1390-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1390-119">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="e1390-119">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




