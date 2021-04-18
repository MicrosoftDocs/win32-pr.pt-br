---
description: Saiba mais sobre o método do Construtor CMediaType. CMediaType (mtype. h). Esse método usa os parâmetros ' mtype ' e ' PHR '.
ms.assetid: b7d5264a-2a5f-4111-96bb-1ea2b13405be
title: Construtor CMediaType. CMediaType (mtype. h)-parâmetros mtype e PHR
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
ms.openlocfilehash: 12ef9012e59dfce1f45d21aa720ae13bd660f2d8
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105811326"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---mtype-and-phr-parameters"></a><span data-ttu-id="c420c-104">Construtor CMediaType. CMediaType (mtype. h)-parâmetros mtype e PHR</span><span class="sxs-lookup"><span data-stu-id="c420c-104">CMediaType.CMediaType constructor (Mtype.h) - mtype and phr parameters</span></span>

<span data-ttu-id="c420c-105">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="c420c-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c420c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c420c-106">Syntax</span></span>


```C++
CMediaType(
  [ref] const AM_MEDIA_TYPE &mtype,
              HRESULT       *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="c420c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c420c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c420c-108">*mtype* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="c420c-108">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c420c-109">Referência a uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="c420c-109">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="c420c-110">O construtor copia o tipo de mídia para o novo objeto, incluindo o bloco de formato, se houver.</span><span class="sxs-lookup"><span data-stu-id="c420c-110">The constructor copies the media type to the new object, including the format block, if any.</span></span>

</dd> <dt>

<span data-ttu-id="c420c-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="c420c-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="c420c-112">Ponteiro para uma variável que recebe um valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="c420c-112">Pointer to a variable that receives an HRESULT value.</span></span> <span data-ttu-id="c420c-113">Esse parâmetro pode ser um ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="c420c-113">This parameter can be a **NULL** pointer.</span></span> <span data-ttu-id="c420c-114">Caso contrário, o chamador deve definir o valor como S \_ OK antes de chamar o construtor.</span><span class="sxs-lookup"><span data-stu-id="c420c-114">Otherwise, the caller must set the value to S\_OK before calling the constructor.</span></span> <span data-ttu-id="c420c-115">Se o Construtor falhar, ele definirá o valor como um código de falha.</span><span class="sxs-lookup"><span data-stu-id="c420c-115">If the constructor fails, it sets the value to a failure code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c420c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c420c-116">Remarks</span></span>

<span data-ttu-id="c420c-117">O construtor chama o método [**CMediaType:: InitMediaType**](cmediatype-initmediatype.md) para inicializar o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="c420c-117">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c420c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c420c-118">Requirements</span></span>

| <span data-ttu-id="c420c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c420c-119">Requirement</span></span>                   | <span data-ttu-id="c420c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c420c-120">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c420c-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c420c-121">Header</span></span>  | <span data-ttu-id="c420c-122">Mtype. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="c420c-122">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="c420c-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c420c-123">Library</span></span> | <span data-ttu-id="c420c-124">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="c420c-124">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="c420c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c420c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c420c-126">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="c420c-126">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




