---
description: Construtor de CEnumMediaTypes. CEnumMediaTypes-método de construtor.
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: Construtor CEnumMediaTypes. CEnumMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d243ed25cc48c5d30d467f97e2ec20e1f0f2b58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095674"
---
# <a name="cenummediatypescenummediatypes-constructor"></a><span data-ttu-id="b53e2-103">Construtor CEnumMediaTypes. CEnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="b53e2-103">CEnumMediaTypes.CEnumMediaTypes constructor</span></span>

<span data-ttu-id="b53e2-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="b53e2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b53e2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b53e2-105">Syntax</span></span>


```C++
CEnumMediaTypes(
   CBasePin        *pPin,
   CEnumMediaTypes *pEnumMediaTypes
);
```



## <a name="parameters"></a><span data-ttu-id="b53e2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b53e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b53e2-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="b53e2-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="b53e2-108">Ponteiro para o PIN no qual a enumeração deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="b53e2-108">Pointer to the pin on which the enumeration is to be performed.</span></span>

</dd> <dt>

<span data-ttu-id="b53e2-109">*pEnumMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="b53e2-109">*pEnumMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="b53e2-110">Ponteiro para a interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) de um enumerador para clonar ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b53e2-110">Pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b53e2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b53e2-111">Remarks</span></span>

<span data-ttu-id="b53e2-112">Se *pEnumMediaTypes* for **NULL**, esse método inicializará o enumerador para o início da sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="b53e2-112">If *pEnumMediaTypes* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="b53e2-113">Caso contrário, ele duplica o estado interno do enumerador especificado por *pEnumMediaTypes*.</span><span class="sxs-lookup"><span data-stu-id="b53e2-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumMediaTypes*.</span></span>

## <a name="requirements"></a><span data-ttu-id="b53e2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b53e2-114">Requirements</span></span>



| <span data-ttu-id="b53e2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b53e2-115">Requirement</span></span> | <span data-ttu-id="b53e2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b53e2-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b53e2-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b53e2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b53e2-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b53e2-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b53e2-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b53e2-119">Library</span></span><br/> | <dl> <span data-ttu-id="b53e2-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b53e2-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b53e2-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b53e2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b53e2-122">**Classe CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="b53e2-122">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




