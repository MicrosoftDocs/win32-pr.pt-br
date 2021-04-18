---
description: O método SetSubtype especifica o subtipo.
ms.assetid: cf52e0dc-d75b-408e-a63c-481d55151d4a
title: Método CMediaType. SetSubtype (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSubtype
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6474777b1b2e91ce0b676fdc7dbd572d7c622f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756815"
---
# <a name="cmediatypesetsubtype-method"></a><span data-ttu-id="7e204-103">Método CMediaType. SetSubtype</span><span class="sxs-lookup"><span data-stu-id="7e204-103">CMediaType.SetSubtype method</span></span>

<span data-ttu-id="7e204-104">O `SetSubtype` método especifica o subtipo.</span><span class="sxs-lookup"><span data-stu-id="7e204-104">The `SetSubtype` method specifies the subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e204-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e204-105">Syntax</span></span>


```C++
void SetSubtype(
   const GUID *psubtype
);
```



## <a name="parameters"></a><span data-ttu-id="7e204-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e204-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e204-107">*psubtype*</span><span class="sxs-lookup"><span data-stu-id="7e204-107">*psubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="7e204-108">Ponteiro para um **GUID** que especifica o subtipo.</span><span class="sxs-lookup"><span data-stu-id="7e204-108">Pointer to a **GUID** that specifies the subtype.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e204-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e204-109">Return value</span></span>

<span data-ttu-id="7e204-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7e204-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e204-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e204-111">Requirements</span></span>



| <span data-ttu-id="7e204-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e204-112">Requirement</span></span> | <span data-ttu-id="7e204-113">Valor</span><span class="sxs-lookup"><span data-stu-id="7e204-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e204-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7e204-114">Header</span></span><br/>  | <dl> <span data-ttu-id="7e204-115"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e204-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="7e204-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7e204-116">Library</span></span><br/> | <dl> <span data-ttu-id="7e204-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7e204-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e204-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e204-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e204-119">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="7e204-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




