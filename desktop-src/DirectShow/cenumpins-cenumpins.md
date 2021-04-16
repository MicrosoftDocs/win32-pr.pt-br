---
description: Método de construtor.
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: Construtor CEnumPins. CEnumPins (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 536782de6992acfc1613d5866f13af658fba6e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750482"
---
# <a name="cenumpinscenumpins-constructor"></a><span data-ttu-id="2c75f-103">Construtor CEnumPins. CEnumPins</span><span class="sxs-lookup"><span data-stu-id="2c75f-103">CEnumPins.CEnumPins constructor</span></span>

<span data-ttu-id="2c75f-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="2c75f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c75f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c75f-105">Syntax</span></span>


```C++
CEnumPins(
   CBaseFilter *pFilter,
   CEnumPins   *pEnumPins
);
```



## <a name="parameters"></a><span data-ttu-id="2c75f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c75f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c75f-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="2c75f-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="2c75f-108">Ponteiro para o filtro no qual enumerar os Pins.</span><span class="sxs-lookup"><span data-stu-id="2c75f-108">Pointer to the filter on which to enumerate the pins.</span></span>

</dd> <dt>

<span data-ttu-id="2c75f-109">*pEnumPins*</span><span class="sxs-lookup"><span data-stu-id="2c75f-109">*pEnumPins*</span></span> 
</dt> <dd>

<span data-ttu-id="2c75f-110">Ponteiro para a interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) de um enumerador para clonar ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2c75f-110">Pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c75f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c75f-111">Remarks</span></span>

<span data-ttu-id="2c75f-112">Se *pEnumPins* for **NULL**, esse método inicializará o enumerador para o início da sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="2c75f-112">If *pEnumPins* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="2c75f-113">Caso contrário, ele duplica o estado interno do enumerador especificado por *pEnumPins*.</span><span class="sxs-lookup"><span data-stu-id="2c75f-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumPins*.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c75f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c75f-114">Requirements</span></span>



| <span data-ttu-id="2c75f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c75f-115">Requirement</span></span> | <span data-ttu-id="2c75f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2c75f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c75f-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c75f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2c75f-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c75f-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2c75f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2c75f-119">Library</span></span><br/> | <dl> <span data-ttu-id="2c75f-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2c75f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c75f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c75f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c75f-122">**Classe CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="2c75f-122">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




