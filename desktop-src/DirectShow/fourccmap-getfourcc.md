---
description: Recupera o&\# 160; DWORD FOURCC do objeto FOURCCMap.
ms.assetid: bb382a57-8499-44c0-b287-2d31f5f5d1d0
title: 'Método FOURCCMap:: GetFOURCC (FOURCC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.GetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c76493ff172f7a5611367fd50aa3b7957cf5441b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747362"
---
# <a name="fourccmapgetfourcc-method"></a><span data-ttu-id="d74a3-103">Método FOURCCMap:: GetFOURCC</span><span class="sxs-lookup"><span data-stu-id="d74a3-103">FOURCCMap::GetFOURCC method</span></span>

<span data-ttu-id="d74a3-104">Recupera o  **DWORD** FOURCC do objeto [**FOURCCMap**](fourccmap.md) .</span><span class="sxs-lookup"><span data-stu-id="d74a3-104">Retrieves the **FOURCC** **DWORD** from the [**FOURCCMap**](fourccmap.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d74a3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d74a3-105">Syntax</span></span>


```C++
DWORD GetFOURCC();
```



## <a name="parameters"></a><span data-ttu-id="d74a3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d74a3-106">Parameters</span></span>

<span data-ttu-id="d74a3-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d74a3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d74a3-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d74a3-108">Return value</span></span>

<span data-ttu-id="d74a3-109">Retorna o valor **DWORD** **FOURCC** .</span><span class="sxs-lookup"><span data-stu-id="d74a3-109">Returns the **FOURCC** **DWORD** value.</span></span> <span data-ttu-id="d74a3-110">Observe que se você construir um **GUID** que não foi originalmente derivado de um **FOURCC**, o valor de retorno será essencialmente aleatório.</span><span class="sxs-lookup"><span data-stu-id="d74a3-110">Note that if you construct a **GUID** that was not originally derived from a **FOURCC**, the return value will be essentially random.</span></span>

## <a name="requirements"></a><span data-ttu-id="d74a3-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d74a3-111">Requirements</span></span>



| <span data-ttu-id="d74a3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d74a3-112">Requirement</span></span> | <span data-ttu-id="d74a3-113">Valor</span><span class="sxs-lookup"><span data-stu-id="d74a3-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d74a3-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d74a3-114">Header</span></span><br/>  | <dl> <span data-ttu-id="d74a3-115"><dt>FourCC. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d74a3-115"><dt>Fourcc.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d74a3-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d74a3-116">Library</span></span><br/> | <dl> <span data-ttu-id="d74a3-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d74a3-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d74a3-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d74a3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d74a3-119">**Classe FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="d74a3-119">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




