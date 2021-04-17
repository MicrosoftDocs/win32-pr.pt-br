---
description: A função DbgTerminate limpa a biblioteca de depuração. Ignorado em compilações de varejo.
ms.assetid: a0e23c57-b4b5-4bcf-8c63-0dee40cc71a7
title: Função DbgTerminate (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgTerminate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d29e5fde86b9573261e39a0dbe2e9d87018ff23c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782200"
---
# <a name="dbgterminate-function"></a><span data-ttu-id="c3d1e-104">Função DbgTerminate</span><span class="sxs-lookup"><span data-stu-id="c3d1e-104">DbgTerminate function</span></span>

<span data-ttu-id="c3d1e-105">A função **DbgTerminate** limpa a biblioteca de depuração.</span><span class="sxs-lookup"><span data-stu-id="c3d1e-105">The **DbgTerminate** function cleans up the debug library.</span></span> <span data-ttu-id="c3d1e-106">Ignorado em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="c3d1e-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d1e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3d1e-107">Syntax</span></span>


```C++
void DbgTerminate(void);
```



## <a name="parameters"></a><span data-ttu-id="c3d1e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3d1e-108">Parameters</span></span>

<span data-ttu-id="c3d1e-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c3d1e-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3d1e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3d1e-110">Return value</span></span>

<span data-ttu-id="c3d1e-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c3d1e-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3d1e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3d1e-112">Remarks</span></span>

<span data-ttu-id="c3d1e-113">Chame essa função se você chamar a função [**DbgInitialise**](dbginitialise.md) .</span><span class="sxs-lookup"><span data-stu-id="c3d1e-113">Call this function if you call the [**DbgInitialise**](dbginitialise.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3d1e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3d1e-114">Requirements</span></span>



| <span data-ttu-id="c3d1e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3d1e-115">Requirement</span></span> | <span data-ttu-id="c3d1e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c3d1e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3d1e-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3d1e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c3d1e-118"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3d1e-118"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c3d1e-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c3d1e-119">Library</span></span><br/> | <dl> <span data-ttu-id="c3d1e-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c3d1e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3d1e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3d1e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3d1e-122">Funções de saída de depuração</span><span class="sxs-lookup"><span data-stu-id="c3d1e-122">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




