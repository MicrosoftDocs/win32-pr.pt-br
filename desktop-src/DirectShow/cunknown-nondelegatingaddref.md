---
description: 'O método NonDelegatingAddRef incrementa a contagem de referência no objeto. Esse método implementa o método INonDelegatingUnknown:: NonDelegatingAddRef.'
ms.assetid: abb6ee51-8fb8-4307-b127-b3667260e35a
title: Método CUnknown. NonDelegatingAddRef (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingAddRef
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f97260c03f0931e94e8ce6de8b7816789b2fe66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752882"
---
# <a name="cunknownnondelegatingaddref-method"></a><span data-ttu-id="95a14-104">Método CUnknown. NonDelegatingAddRef</span><span class="sxs-lookup"><span data-stu-id="95a14-104">CUnknown.NonDelegatingAddRef method</span></span>

<span data-ttu-id="95a14-105">O `NonDelegatingAddRef` método incrementa a contagem de referência no objeto.</span><span class="sxs-lookup"><span data-stu-id="95a14-105">The `NonDelegatingAddRef` method increments the reference count on the object.</span></span> <span data-ttu-id="95a14-106">Esse método implementa o método **INonDelegatingUnknown:: NonDelegatingAddRef** .</span><span class="sxs-lookup"><span data-stu-id="95a14-106">This method implements the **INonDelegatingUnknown::NonDelegatingAddRef** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="95a14-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95a14-107">Syntax</span></span>


```C++
ULONG NonDelegatingAddRef();
```



## <a name="parameters"></a><span data-ttu-id="95a14-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95a14-108">Parameters</span></span>

<span data-ttu-id="95a14-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="95a14-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="95a14-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95a14-110">Return value</span></span>

<span data-ttu-id="95a14-111">Retorna a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="95a14-111">Returns the reference count.</span></span>

## <a name="requirements"></a><span data-ttu-id="95a14-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95a14-112">Requirements</span></span>



| <span data-ttu-id="95a14-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="95a14-113">Requirement</span></span> | <span data-ttu-id="95a14-114">Valor</span><span class="sxs-lookup"><span data-stu-id="95a14-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95a14-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95a14-115">Header</span></span><br/>  | <dl> <span data-ttu-id="95a14-116"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95a14-116"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="95a14-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95a14-117">Library</span></span><br/> | <dl> <span data-ttu-id="95a14-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="95a14-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




