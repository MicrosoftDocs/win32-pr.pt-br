---
description: Método destruidor.
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
ms.openlocfilehash: fa27d50a9c1acbc9c8a27407cb97673d60158e4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748193"
---
# <a name="csourcestreamcsourcestream-destructor"></a><span data-ttu-id="32a61-103">Destruidor CSourceStream. ~ CSourceStream</span><span class="sxs-lookup"><span data-stu-id="32a61-103">CSourceStream.~CSourceStream destructor</span></span>

<span data-ttu-id="32a61-104">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="32a61-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="32a61-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32a61-105">Syntax</span></span>


```C++
~CSourceStream();
```



## <a name="remarks"></a><span data-ttu-id="32a61-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="32a61-106">Remarks</span></span>

<span data-ttu-id="32a61-107">O destruidor remove automaticamente o PIN do filtro proprietário, chamando [**CSource:: RemovePin**](csource-removepin.md).</span><span class="sxs-lookup"><span data-stu-id="32a61-107">The destructor automatically removes the pin from the owning filter, by calling [**CSource::RemovePin**](csource-removepin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32a61-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32a61-108">Requirements</span></span>



| <span data-ttu-id="32a61-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="32a61-109">Requirement</span></span> | <span data-ttu-id="32a61-110">Valor</span><span class="sxs-lookup"><span data-stu-id="32a61-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32a61-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32a61-111">Header</span></span><br/>  | <dl> <span data-ttu-id="32a61-112"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32a61-112"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="32a61-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="32a61-113">Library</span></span><br/> | <dl> <span data-ttu-id="32a61-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="32a61-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32a61-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="32a61-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32a61-116">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="32a61-116">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




