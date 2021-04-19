---
description: O método set define o tipo de mídia de outro tipo de mídia.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: Método CMediaType. Set (mtype. h)-parâmetro mtype [REF]
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
ms.openlocfilehash: e8fd9145ee33dbe4b589b34833836466efa62ada
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389084"
---
# <a name="cmediatypeset-method-mtypeh"></a><span data-ttu-id="0ebbd-103">Método CMediaType. Set (mtype. h)</span><span class="sxs-lookup"><span data-stu-id="0ebbd-103">CMediaType.Set method (Mtype.h)</span></span>

<span data-ttu-id="0ebbd-104">O `Set` método define o tipo de mídia de outro tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="0ebbd-104">The `Set` method sets the media type from another media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ebbd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ebbd-105">Syntax</span></span>


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="0ebbd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ebbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ebbd-107">*mtype* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="0ebbd-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="0ebbd-108">Referência a uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="0ebbd-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ebbd-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0ebbd-109">Return value</span></span>

<span data-ttu-id="0ebbd-110">Retorna S \_ OK ou E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0ebbd-110">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ebbd-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ebbd-111">Remarks</span></span>

<span data-ttu-id="0ebbd-112">Esse método copia todo o tipo de mídia de *mtype*.</span><span class="sxs-lookup"><span data-stu-id="0ebbd-112">This method copies the entire media type from *mtype*.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ebbd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ebbd-113">Requirements</span></span>



| <span data-ttu-id="0ebbd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ebbd-114">Requirement</span></span> | <span data-ttu-id="0ebbd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0ebbd-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ebbd-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0ebbd-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0ebbd-117"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ebbd-117"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="0ebbd-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ebbd-118">Library</span></span><br/> | <dl> <span data-ttu-id="0ebbd-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0ebbd-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ebbd-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ebbd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ebbd-121">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="0ebbd-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




