---
description: O método getamostrate recupera o tamanho da amostra.
ms.assetid: 5cc98556-cca6-46ca-ad33-cd40011ff6f4
title: Método CMediaType. getsampleize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.GetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc5b80e20ad2a16af9c25c68499348ffa744c0fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769227"
---
# <a name="cmediatypegetsamplesize-method"></a><span data-ttu-id="274bf-103">Método CMediaType. getsampleize</span><span class="sxs-lookup"><span data-stu-id="274bf-103">CMediaType.GetSampleSize method</span></span>

<span data-ttu-id="274bf-104">O `GetSampleSize` método recupera o tamanho da amostra.</span><span class="sxs-lookup"><span data-stu-id="274bf-104">The `GetSampleSize` method retrieves the sample size.</span></span>

## <a name="syntax"></a><span data-ttu-id="274bf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="274bf-105">Syntax</span></span>


```C++
ULONG GetSampleSize() const;
```



## <a name="parameters"></a><span data-ttu-id="274bf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="274bf-106">Parameters</span></span>

<span data-ttu-id="274bf-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="274bf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="274bf-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="274bf-108">Return value</span></span>

<span data-ttu-id="274bf-109">Se o tamanho da amostra for fixo, o retornará o tamanho da amostra em bytes.</span><span class="sxs-lookup"><span data-stu-id="274bf-109">If the sample size is fixed, returns the sample size in bytes.</span></span> <span data-ttu-id="274bf-110">Caso contrário, retornará zero.</span><span class="sxs-lookup"><span data-stu-id="274bf-110">Otherwise, returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="274bf-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="274bf-111">Requirements</span></span>



| <span data-ttu-id="274bf-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="274bf-112">Requirement</span></span> | <span data-ttu-id="274bf-113">Valor</span><span class="sxs-lookup"><span data-stu-id="274bf-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="274bf-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="274bf-114">Header</span></span><br/>  | <dl> <span data-ttu-id="274bf-115"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="274bf-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="274bf-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="274bf-116">Library</span></span><br/> | <dl> <span data-ttu-id="274bf-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="274bf-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="274bf-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="274bf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="274bf-119">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="274bf-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




