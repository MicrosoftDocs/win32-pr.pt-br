---
description: CSourceStream. ~ CSourceStream destruidor-método Destruitor.
ms.assetid: 678085c2-5999-4e62-8749-99b783787cc6
title: Destruidor CSourceStream. ~ CSourceStream (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.~CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbf53184dadc42145758ab387d15e8b0a1bfe09d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085204"
---
# <a name="csourcestreamcsourcestream-destructor"></a><span data-ttu-id="78a7f-103">Destruidor CSourceStream. ~ CSourceStream</span><span class="sxs-lookup"><span data-stu-id="78a7f-103">CSourceStream.~CSourceStream destructor</span></span>

<span data-ttu-id="78a7f-104">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="78a7f-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="78a7f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78a7f-105">Syntax</span></span>


```C++
~CSourceStream();
```



## <a name="remarks"></a><span data-ttu-id="78a7f-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="78a7f-106">Remarks</span></span>

<span data-ttu-id="78a7f-107">O destruidor remove automaticamente o PIN do filtro proprietário, chamando [**CSource:: RemovePin**](csource-removepin.md).</span><span class="sxs-lookup"><span data-stu-id="78a7f-107">The destructor automatically removes the pin from the owning filter, by calling [**CSource::RemovePin**](csource-removepin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78a7f-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78a7f-108">Requirements</span></span>



| <span data-ttu-id="78a7f-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="78a7f-109">Requirement</span></span> | <span data-ttu-id="78a7f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="78a7f-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78a7f-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78a7f-111">Header</span></span><br/>  | <dl> <span data-ttu-id="78a7f-112"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78a7f-112"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="78a7f-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="78a7f-113">Library</span></span><br/> | <dl> <span data-ttu-id="78a7f-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="78a7f-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78a7f-115">Consulte também</span><span class="sxs-lookup"><span data-stu-id="78a7f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78a7f-116">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="78a7f-116">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




