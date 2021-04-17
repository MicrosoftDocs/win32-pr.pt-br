---
description: 'Decrementa a contagem de referência no objeto. Esse método implementa o método INonDelegatingUnknown:: NonDelegatingRelease.'
ms.assetid: 58610f7d-5524-450f-a0f8-b299944abc78
title: Método CUnknown. NonDelegatingRelease (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingRelease
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec709d4b636eea6a145f9a24a868ad5c495e4477
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754217"
---
# <a name="cunknownnondelegatingrelease-method"></a><span data-ttu-id="b2755-104">Método CUnknown. NonDelegatingRelease</span><span class="sxs-lookup"><span data-stu-id="b2755-104">CUnknown.NonDelegatingRelease method</span></span>

<span data-ttu-id="b2755-105">Decrementa a contagem de referência no objeto.</span><span class="sxs-lookup"><span data-stu-id="b2755-105">Decrements the reference count on the object.</span></span> <span data-ttu-id="b2755-106">Esse método implementa o método **INonDelegatingUnknown:: NonDelegatingRelease** .</span><span class="sxs-lookup"><span data-stu-id="b2755-106">This method implements the **INonDelegatingUnknown::NonDelegatingRelease** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2755-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2755-107">Syntax</span></span>


```C++
ULONG NonDelegatingRelease();
```



## <a name="parameters"></a><span data-ttu-id="b2755-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2755-108">Parameters</span></span>

<span data-ttu-id="b2755-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b2755-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b2755-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2755-110">Return value</span></span>

<span data-ttu-id="b2755-111">Retorna a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="b2755-111">Returns the reference count.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2755-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2755-112">Remarks</span></span>

<span data-ttu-id="b2755-113">Quando a contagem de referência chega a zero, o objeto se exclui.</span><span class="sxs-lookup"><span data-stu-id="b2755-113">When the reference count reaches zero, the object deletes itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2755-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2755-114">Requirements</span></span>



| <span data-ttu-id="b2755-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2755-115">Requirement</span></span> | <span data-ttu-id="b2755-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b2755-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2755-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2755-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b2755-118"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2755-118"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b2755-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2755-119">Library</span></span><br/> | <dl> <span data-ttu-id="b2755-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b2755-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




