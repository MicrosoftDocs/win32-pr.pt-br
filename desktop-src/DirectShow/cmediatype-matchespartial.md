---
description: O método MatchesPartial determina se esse tipo de mídia corresponde a um tipo de mídia parcialmente especificado.
ms.assetid: 62d531f3-5aa2-4af2-b951-584a49a849fc
title: Método CMediaType. MatchesPartial (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.MatchesPartial
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4d2d4232b64857ca209e6b43cd7081a42495fee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756621"
---
# <a name="cmediatypematchespartial-method"></a><span data-ttu-id="5f07d-103">Método CMediaType. MatchesPartial</span><span class="sxs-lookup"><span data-stu-id="5f07d-103">CMediaType.MatchesPartial method</span></span>

<span data-ttu-id="5f07d-104">O `MatchesPartial` método determina se esse tipo de mídia corresponde a um tipo de mídia parcialmente especificado.</span><span class="sxs-lookup"><span data-stu-id="5f07d-104">The `MatchesPartial` method determines if this media type matches a partially specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f07d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f07d-105">Syntax</span></span>


```C++
BOOL MatchesPartial(
   const CMediaType *ppartial
) const;
```



## <a name="parameters"></a><span data-ttu-id="5f07d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f07d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f07d-107">*ppartial*</span><span class="sxs-lookup"><span data-stu-id="5f07d-107">*ppartial*</span></span> 
</dt> <dd>

<span data-ttu-id="5f07d-108">Ponteiro para o tipo de mídia a ser correspondido.</span><span class="sxs-lookup"><span data-stu-id="5f07d-108">Pointer to the media type to match.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f07d-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f07d-109">Return value</span></span>

<span data-ttu-id="5f07d-110">Retornará **true** se os tipos de mídia corresponderem.</span><span class="sxs-lookup"><span data-stu-id="5f07d-110">Returns **TRUE** if the media types match.</span></span> <span data-ttu-id="5f07d-111">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="5f07d-111">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f07d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f07d-112">Remarks</span></span>

<span data-ttu-id="5f07d-113">O tipo de mídia especificado por *ppartial* pode ter um valor de GUID \_ NULL para o tipo principal, subtipo ou formato.</span><span class="sxs-lookup"><span data-stu-id="5f07d-113">The media type specified by *ppartial* can have a value of GUID\_NULL for the major type, subtype, or format type.</span></span> <span data-ttu-id="5f07d-114">Todos os membros com \_ valores nulos de GUID não são testados.</span><span class="sxs-lookup"><span data-stu-id="5f07d-114">Any members with GUID\_NULL values are not tested.</span></span> <span data-ttu-id="5f07d-115">(Em vigor, GUID \_ NULL atua como um curinga.) Os membros com valores diferentes de GUID \_ NULL devem corresponder ao tipo de mídia a ser correspondido.</span><span class="sxs-lookup"><span data-stu-id="5f07d-115">(In effect, GUID\_NULL acts as a wildcard.) Members with values other than GUID\_NULL must match for the media type to match.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f07d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f07d-116">Requirements</span></span>



| <span data-ttu-id="5f07d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f07d-117">Requirement</span></span> | <span data-ttu-id="5f07d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5f07d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f07d-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f07d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5f07d-120"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f07d-120"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="5f07d-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5f07d-121">Library</span></span><br/> | <dl> <span data-ttu-id="5f07d-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5f07d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f07d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f07d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f07d-124">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="5f07d-124">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




