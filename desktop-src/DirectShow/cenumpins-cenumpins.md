---
description: Construtor de CEnumPins. CEnumPins-método de construtor.
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
ms.openlocfilehash: caa27dfe0190df15be1e41b7128c06249f1ae2b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099224"
---
# <a name="cenumpinscenumpins-constructor"></a><span data-ttu-id="dbd23-103">Construtor CEnumPins. CEnumPins</span><span class="sxs-lookup"><span data-stu-id="dbd23-103">CEnumPins.CEnumPins constructor</span></span>

<span data-ttu-id="dbd23-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="dbd23-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbd23-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dbd23-105">Syntax</span></span>


```C++
CEnumPins(
   CBaseFilter *pFilter,
   CEnumPins   *pEnumPins
);
```



## <a name="parameters"></a><span data-ttu-id="dbd23-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbd23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbd23-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="dbd23-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="dbd23-108">Ponteiro para o filtro no qual enumerar os Pins.</span><span class="sxs-lookup"><span data-stu-id="dbd23-108">Pointer to the filter on which to enumerate the pins.</span></span>

</dd> <dt>

<span data-ttu-id="dbd23-109">*pEnumPins*</span><span class="sxs-lookup"><span data-stu-id="dbd23-109">*pEnumPins*</span></span> 
</dt> <dd>

<span data-ttu-id="dbd23-110">Ponteiro para a interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) de um enumerador para clonar ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dbd23-110">Pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbd23-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbd23-111">Remarks</span></span>

<span data-ttu-id="dbd23-112">Se *pEnumPins* for **NULL**, esse método inicializará o enumerador para o início da sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="dbd23-112">If *pEnumPins* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="dbd23-113">Caso contrário, ele duplica o estado interno do enumerador especificado por *pEnumPins*.</span><span class="sxs-lookup"><span data-stu-id="dbd23-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumPins*.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbd23-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbd23-114">Requirements</span></span>



| <span data-ttu-id="dbd23-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbd23-115">Requirement</span></span> | <span data-ttu-id="dbd23-116">Valor</span><span class="sxs-lookup"><span data-stu-id="dbd23-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbd23-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dbd23-117">Header</span></span><br/>  | <dl> <span data-ttu-id="dbd23-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dbd23-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dbd23-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dbd23-119">Library</span></span><br/> | <dl> <span data-ttu-id="dbd23-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="dbd23-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbd23-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="dbd23-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbd23-122">**Classe CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="dbd23-122">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




