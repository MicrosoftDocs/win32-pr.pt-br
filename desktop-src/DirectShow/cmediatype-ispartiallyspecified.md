---
description: O método IsPartiallySpecified determina se o tipo de mídia está parcialmente definido. Um tipo de mídia será parcial se o tipo de tipo principal, subtipo ou formato for GUID \_ NULL.
ms.assetid: 26dd7a2b-b2f8-485f-a9af-31c3a9eb1def
title: Método CMediaType. IsPartiallySpecified (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsPartiallySpecified
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32c39942ab3f97d45ecf71ba841d56b7afd4be62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759313"
---
# <a name="cmediatypeispartiallyspecified-method"></a><span data-ttu-id="da362-104">Método CMediaType. IsPartiallySpecified</span><span class="sxs-lookup"><span data-stu-id="da362-104">CMediaType.IsPartiallySpecified method</span></span>

<span data-ttu-id="da362-105">O `IsPartiallySpecified` método determina se o tipo de mídia está parcialmente definido.</span><span class="sxs-lookup"><span data-stu-id="da362-105">The `IsPartiallySpecified` method determines if the media type is partially defined.</span></span> <span data-ttu-id="da362-106">Um tipo de mídia será *parcial* se o tipo de tipo principal, subtipo ou formato for GUID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="da362-106">A media type is *partial* if the major type, subtype, or format type is GUID\_NULL.</span></span>

## <a name="syntax"></a><span data-ttu-id="da362-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da362-107">Syntax</span></span>


```C++
BOOL IsPartiallySpecified() const;
```



## <a name="parameters"></a><span data-ttu-id="da362-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da362-108">Parameters</span></span>

<span data-ttu-id="da362-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="da362-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="da362-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="da362-110">Return value</span></span>

<span data-ttu-id="da362-111">Retornará **true** se o tipo de mídia for especificado parcialmente.</span><span class="sxs-lookup"><span data-stu-id="da362-111">Returns **TRUE** if the media type is partially specified.</span></span> <span data-ttu-id="da362-112">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="da362-112">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="da362-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="da362-113">Remarks</span></span>

<span data-ttu-id="da362-114">O método [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) pode aceitar tipos de mídia parciais.</span><span class="sxs-lookup"><span data-stu-id="da362-114">The [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method can accept partial media types.</span></span>

<span data-ttu-id="da362-115">A implementação, na verdade, não testa o subtipo.</span><span class="sxs-lookup"><span data-stu-id="da362-115">The implementation does not actually test the subtype.</span></span> <span data-ttu-id="da362-116">Se houver um tipo de formato especificado, o tipo de mídia não será considerado parcial, mesmo que o subtipo seja \_ nulo como GUID.</span><span class="sxs-lookup"><span data-stu-id="da362-116">If there is a specified format type, the media type is not considered partial, even if the subtype is GUID\_NULL.</span></span>

## <a name="requirements"></a><span data-ttu-id="da362-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da362-117">Requirements</span></span>



| <span data-ttu-id="da362-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="da362-118">Requirement</span></span> | <span data-ttu-id="da362-119">Valor</span><span class="sxs-lookup"><span data-stu-id="da362-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da362-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="da362-120">Header</span></span><br/>  | <dl> <span data-ttu-id="da362-121"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da362-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="da362-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="da362-122">Library</span></span><br/> | <dl> <span data-ttu-id="da362-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="da362-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da362-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="da362-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da362-125">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="da362-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




