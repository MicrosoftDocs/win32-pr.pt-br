---
description: Saiba mais sobre o método do Construtor CMediaType. CMediaType (mtype. h). Esse método usa o parâmetro ' majortype '.
ms.assetid: 89356578-0509-46c1-abd4-421688017f1d
title: Construtor CMediaType. CMediaType (mtype. h)-parâmetro majortype
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a99717e41424a99b3c1e79674426fb14c5b57b9d
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105759137"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---majortype-parameter"></a><span data-ttu-id="c0cc5-104">Construtor CMediaType. CMediaType (mtype. h)-parâmetro majortype</span><span class="sxs-lookup"><span data-stu-id="c0cc5-104">CMediaType.CMediaType constructor (Mtype.h) - majortype parameter</span></span>

<span data-ttu-id="c0cc5-105">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="c0cc5-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0cc5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0cc5-106">Syntax</span></span>


```C++
CMediaType(
   const GUID *majortype
);
```



## <a name="parameters"></a><span data-ttu-id="c0cc5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0cc5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0cc5-108">*majortype*</span><span class="sxs-lookup"><span data-stu-id="c0cc5-108">*majortype*</span></span> 
</dt> <dd>

<span data-ttu-id="c0cc5-109">Ponteiro para um **GUID** de tipo principal.</span><span class="sxs-lookup"><span data-stu-id="c0cc5-109">Pointer to a major type **GUID**.</span></span> <span data-ttu-id="c0cc5-110">O construtor inicializa o GUID de tipo principal para esse valor.</span><span class="sxs-lookup"><span data-stu-id="c0cc5-110">The constructor initializes the major type GUID to this value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0cc5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0cc5-111">Remarks</span></span>

<span data-ttu-id="c0cc5-112">O construtor chama o método [**CMediaType:: InitMediaType**](cmediatype-initmediatype.md) para inicializar o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="c0cc5-112">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0cc5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0cc5-113">Requirements</span></span>

| <span data-ttu-id="c0cc5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0cc5-114">Requirement</span></span>                   | <span data-ttu-id="c0cc5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c0cc5-115">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0cc5-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0cc5-116">Header</span></span>  | <span data-ttu-id="c0cc5-117">Mtype. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="c0cc5-117">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="c0cc5-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0cc5-118">Library</span></span> | <span data-ttu-id="c0cc5-119">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="c0cc5-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="c0cc5-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0cc5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0cc5-121">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="c0cc5-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




