---
description: O método CMediaType. Set (mtype. h) define o tipo de mídia de outro tipo de mídia. O método usa o parâmetro ' cmtype '.
ms.assetid: 71c19d0f-93b6-41db-8659-c64411b83e7c
title: Método CMediaType. Set (mtype. h)-cmtype [REF] parâmetro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9bf14132660045afbd171173a38d3ea320ba1aa
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105756620"
---
# <a name="cmediatypeset-method-mtypeh---cmtype-ref-parameter"></a><span data-ttu-id="3d1d3-104">Método CMediaType. Set (mtype. h)-cmtype [REF] parâmetro</span><span class="sxs-lookup"><span data-stu-id="3d1d3-104">CMediaType.Set method (Mtype.h) - cmtype [ref] parameter</span></span>

<span data-ttu-id="3d1d3-105">O `Set` método define o tipo de mídia de outro tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="3d1d3-105">The `Set` method sets the media type from another media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d1d3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d1d3-106">Syntax</span></span>


```C++
HRESULT Set(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a><span data-ttu-id="3d1d3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d1d3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d1d3-108">*cmtype* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="3d1d3-108">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3d1d3-109">Referência a um objeto [**CMediaType**](cmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="3d1d3-109">Reference to a [**CMediaType**](cmediatype.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d1d3-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3d1d3-110">Return value</span></span>

<span data-ttu-id="3d1d3-111">Retorna S \_ OK ou E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3d1d3-111">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d1d3-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d1d3-112">Remarks</span></span>

<span data-ttu-id="3d1d3-113">Esse método copia todo o tipo de mídia de *cmtype*.</span><span class="sxs-lookup"><span data-stu-id="3d1d3-113">This method copies the entire media type from *cmtype*.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d1d3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d1d3-114">Requirements</span></span>

| <span data-ttu-id="3d1d3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d1d3-115">Requirement</span></span>                   | <span data-ttu-id="3d1d3-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3d1d3-116">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d1d3-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3d1d3-117">Header</span></span>  | <span data-ttu-id="3d1d3-118">Mtype. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="3d1d3-118">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="3d1d3-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3d1d3-119">Library</span></span> | <span data-ttu-id="3d1d3-120">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="3d1d3-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="3d1d3-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d1d3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d1d3-122">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="3d1d3-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




