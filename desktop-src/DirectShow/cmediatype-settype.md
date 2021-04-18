---
description: O método SetType especifica o tipo principal.
ms.assetid: 3fd93d5e-73ea-453e-8f08-652d5a81239f
title: Método CMediaType. SetType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfcf6ca634bce92701eb89f26dcfb6bdfb51f698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771850"
---
# <a name="cmediatypesettype-method"></a><span data-ttu-id="e8cbc-103">Método CMediaType. SetType</span><span class="sxs-lookup"><span data-stu-id="e8cbc-103">CMediaType.SetType method</span></span>

<span data-ttu-id="e8cbc-104">O `SetType` método especifica o tipo principal.</span><span class="sxs-lookup"><span data-stu-id="e8cbc-104">The `SetType` method specifies the major type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8cbc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8cbc-105">Syntax</span></span>


```C++
void SetType(
   const GUID *ptype
);
```



## <a name="parameters"></a><span data-ttu-id="e8cbc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8cbc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8cbc-107">*ptype*</span><span class="sxs-lookup"><span data-stu-id="e8cbc-107">*ptype*</span></span> 
</dt> <dd>

<span data-ttu-id="e8cbc-108">Ponteiro para um **GUID** que especifica o tipo principal.</span><span class="sxs-lookup"><span data-stu-id="e8cbc-108">Pointer to a **GUID** that specifies the major type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8cbc-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8cbc-109">Return value</span></span>

<span data-ttu-id="e8cbc-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e8cbc-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8cbc-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8cbc-111">Requirements</span></span>



| <span data-ttu-id="e8cbc-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8cbc-112">Requirement</span></span> | <span data-ttu-id="e8cbc-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e8cbc-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8cbc-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e8cbc-114">Header</span></span><br/>  | <dl> <span data-ttu-id="e8cbc-115"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8cbc-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="e8cbc-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8cbc-116">Library</span></span><br/> | <dl> <span data-ttu-id="e8cbc-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e8cbc-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8cbc-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8cbc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8cbc-119">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="e8cbc-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




